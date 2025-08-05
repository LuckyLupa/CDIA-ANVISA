# Projeto-CDIA

Automação Inteligente de Relatórios de Fiscalização Administrativa com uso de IA  
**Aplicado aos contratos de portos, aeroportos e engenharia da GELOG/GGGAF/Anvisa**

---

## 📌 Objetivo

Este projeto visa aplicar técnicas de **Inteligência Artificial** e **Processamento de Linguagem Natural (NLP)** para automatizar a geração de **relatórios administrativos de fiscalização**, a partir de faturas em PDF recebidas pela Anvisa. O objetivo é reduzir o tempo operacional, padronizar documentos e mitigar erros manuais na rotina da GELOG.

---

## 🗂️ Estrutura do Projeto

```
Projeto-CDIA/
│
├── data/                      # Dados de entrada e saída
│   ├── faturas/               # Faturas reais em PDF
│   ├── contratos/             # Termos de cessão ou documentos auxiliares
│   └── exemplos_saida/        # Relatórios já gerados (manual e automático)
│
├── src/                       # Scripts de processamento
│   ├── extrator_ocr.py        # Leitura OCR de PDFs
│   ├── classificador_nlp.py   # Classificação e estruturação de dados textuais
│   ├── gerador_relatorio.py   # Geração de relatórios a partir do template
│   └── interface_streamlit.py # (Opcional) Interface web para teste do fluxo
│
├── templates/                 # Modelos de relatório (.odt)
│   └── modelo_relatorio.odt
│
├── apresentacao/              # Slides usados nas bancas
│   └── slides_projeto.pdf
│
├── tcc/                       # Artigo final e textos do TCC
│   └── documento_final.docx
│
└── README.md                  # Este arquivo
```

---

## 🧰 Tecnologias e Ferramentas

- **Python 3.10+**
- `pytesseract` + `pdf2image` (OCR)
- `spaCy` ou `transformers` (para NLP)
- `odfpy` ou `docxtpl` (para preencher modelos de relatório)
- `Streamlit` (opcional, para visualização simples)
- **LibreOffice** ou **OnlyOffice** (compatibilidade com `.odt`)

---

## 🚀 Como executar

1. Instale os requisitos:
   ```bash
   pip install -r requirements.txt
   ```

2. Execute o pipeline principal:
   ```bash
   python src/main.py
   ```

3. (Opcional) Inicie a interface:
   ```bash
   streamlit run src/interface_streamlit.py
   ```

---

## 👤 Autor

**Luciano Magno de Araújo**  
Pós-graduação em Ciência de Dados e Inteligência Artificial – CDIA/PROADI  
Anvisa – GELOG/GGGAF

---

## 🗓️ Cronograma

- 📌 **1ª orientação:** 11–16/08  
- 🛠️ **Pré-banca:** 15/09  
- 🎤 **Apresentação:** 16–26/09  
- 📩 **Entrega final (projeto + pôster):** 26/10  
