# GhostEAD – Caçador de cursos fantasmas (`tool_ghostead`)

Plugin de administração para Moodle que encontra **cursos fantasmas** (abandonados, vazios ou sem uso) e permite **ocultar** ou **arquivar** em lote, de forma segura e reversível.

> Status: **0.2.0 – alpha**. Teste em ambiente de homologação antes de usar em produção.
>
> Compatibilidade: **Moodle 3.7 ou superior** (PHP 7.1+). O código evita sintaxe de PHP mais novo para rodar em instalações antigas.

## Como funciona

Cada curso recebe um **índice fantasma de 0 a 100**:

| Sinal | Pontos |
|---|---|
| Sem acesso na janela de inatividade (padrão: 6 meses) | 40 |
| Sem alunos | 25 |
| Sem professores | 15 |
| Curso vazio (até 1 atividade, o fórum de avisos automático) | 20 |

Só aparecem na lista cursos com pontuação ≥ mínimo configurado (padrão 60). Cursos criados há menos de 30 dias são ignorados.
