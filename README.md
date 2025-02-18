# Calendario-em-Batch-File

**Objetivo**:  
Este script tem como objetivo calcular o número de dias em um mês específico de um ano, levando em consideração se o ano é bissexto ou não. Após calcular o número de dias, o script cria uma pasta para cada dia do mês dentro de uma estrutura de diretórios fornecida como entrada. O script resolve o problema de determinar a quantidade de dias de cada mês e gera uma organização de pastas representando cada dia.

**O que ele realiza**:
1. **Calcula o número de dias no mês**: O script verifica se o ano é bissexto e, com isso, define corretamente o número de dias para cada mês, levando em conta que fevereiro tem 29 dias nos anos bissextos e 28 dias nos outros anos.
2. **Cria diretórios**: Para cada dia do mês, o script cria uma pasta dentro da estrutura de diretórios especificada.
3. **Verifica se o ano é bissexto**: O script calcula se o ano é bissexto (ano divisível por 4, mas não por 100, ou divisível por 400) para ajustar o número de dias em fevereiro.

---

## Explicação Detalhada do Código

### 1. Verificação e Criação de Diretórios
```batch
if not exist "%1" (
    mkdir "%1"
)
cd "%1"

if not exist "%2" (
    mkdir "%2"
)
cd "%2"
