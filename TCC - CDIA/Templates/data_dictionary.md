# Dicionário de Dados - Projeto CDIA

Este documento descreve os campos utilizados no relatório auxiliar automatizado, 
indicando a origem, tipo e exemplos de preenchimento. 
Serve como referência para o pipeline de automação.

---

## 📌 Campos Fixos (pré-preenchidos)

| Campo                  | Valor Padrão                                    | Observações |
|------------------------|------------------------------------------------|-------------|
| UOD                   | Gerência de Logística / GELOG                   | Sempre fixo |
| Processo SEI           | 25351.939296/2020-53                           | Definido por contrato |
| Processo Administrativo| 25752.905099/2019-84                           | Definido por contrato |
| Nº do Contrato         | 2204/2019                                      | Definido por contrato |
| Contratada             | CONCESSIONÁRIA AEROPORTO RIO DE JANEIRO S.A.   | Sempre fixo |
| Objeto                 | Cessão de uso de espaço para serviços de TIC no AIRJ | Sempre fixo |
| Conclusão Padrão       | Que os serviços foram prestados de forma satisfatória. | Texto fixo, editável se necessário |

---

## 📌 Campos Variáveis (extraídos da fatura)

| Campo                  | Placeholder           | Fonte             | Exemplo         |
|------------------------|-----------------------|------------------|-----------------|
| Número da Fatura       | {{NUM_FATURA}}        | Fatura PDF        | 8000475862      |
| Data de Emissão        | {{DATA_EMISSAO}}      | Fatura PDF        | 25/06/2025      |
| Data de Vencimento     | {{DATA_VENCIMENTO}}   | Fatura PDF        | 20/07/2025      |
| Período de Competência | {{PERIODO}}           | Manual / Nome do arquivo | Julho/2025 |
| CNPJ Concessionária    | {{CNPJ_CONCESSIONARIA}} | Fatura PDF      | 19.726.111/0001-08 |
| Valor Custo Operacional TI | {{VALOR_CUSTO_TI}} | Fatura PDF      | 11.179,62       |
| Valor Consumo TI       | {{VALOR_CONSUMO_TI}}  | Fatura PDF        | 169,99          |
| Valor Total Bruto      | {{VALOR_TOTAL_BRUTO}} | Soma das rubricas | 11.349,61       |

---

## 📌 Campos Adicionais para Controle Interno

| Campo                  | Placeholder            | Fonte                  | Exemplo                          |
|------------------------|------------------------|------------------------|----------------------------------|
| Número do Empenho      | {{NUM_EMPENHO}}        | GEFIC / SIASG          | 2025NE000123                     |
| ID no contratos.gov.br | {{ID_CONTRATOS_GOV}}   | contratos.gov.br       | 123456                           |
| Link do PDF da Fatura  | {{LINK_FATURA}}        | Sistema Interno / SEI  | https://sei.anvisa.gov/fatura.pdf|
| Hash SHA256 do PDF     | {{HASH_PDF}}           | Gerado pelo script     | a3f5c8d... (64 caracteres)       |

---

## 📝 Observação Final

Este dicionário será atualizado à medida que novos campos forem incluídos no pipeline. 
Ele deve ser usado como guia tanto para a automação em Python quanto para a validação manual pelo fiscal.
