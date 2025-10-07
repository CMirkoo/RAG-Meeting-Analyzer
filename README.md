# 🤖 RAG-Meeting-Analyzer: Riassunto e Assegnazione Attività da Trascrizioni

Questo progetto dimostra l'uso di **Large Language Models (LLM)** e della tecnica **Retrieval-Augmented Generation (RAG)** per analizzare trascrizioni di meeting non strutturate, generando automaticamente un riassunto conciso e un elenco strutturato delle attività assegnate.

---

## 🚀 Stack Tecnologico

* **LlamaIndex:** Utilizzato per l'indicizzazione dei documenti e l'implementazione del **motore di query RAG** per una estrazione di informazioni più mirata.
* **LangChain / OpenAI:** Fornisce l'interfaccia per interagire con i modelli LLM (es. GPT-4.1-mini) per la sintesi e l'estrazione di dati.
* **Python:** Linguaggio principale per lo scripting e l'automazione.
* **Requests:** Utilizzato per il download dinamico dei file di trascrizione.

---

## ✨ Caratteristiche Principali

Il progetto realizza uno script Python che esegue i seguenti passaggi chiave:

1.  **Download Dinamico:** Recupera la trascrizione del meeting da un URL remoto e la salva localmente.
2.  **Indicizzazione RAG:** Utilizza LlamaIndex per suddividere il testo in chunk e indicizzarlo (Vector Store Index), preparando il documento per query specifiche.
3.  **Generazione Riassunto:** Interroga l'indice per produrre un **riassunto puntato** dei punti principali discussi.
4.  **Estrazione Attività:** Interroga l'indice con un prompt mirato per **identificare chiaramente le attività assegnate**, specificando il nome e cognome del responsabile per ciascuna.

---

## 💡 Obiettivi Raggiunti

* **Efficienza:** Automatizza l'analisi post-meeting, riducendo il tempo speso per l'elaborazione manuale.
* **Accuratezza:** Sfrutta la potenza dell'LLM, supportata dal contesto RAG, per estrarre informazioni chiave con elevata precisione.
* **Struttura:** Trasforma il testo libero in output strutturato e immediatamente utilizzabile (riassunti e liste di compiti).

---

## ⚙️ Come Eseguire il Progetto

### Prerequisiti

È necessario avere una chiave **API OpenAI** valida.

1.  **Configura l'API:**
    Nel file principale dello script, inserisci la tua chiave API OpenAI.
    ```python
    # Imposta API OpenAI
    os.environ["OPENAI_API_KEY"] = "TUA_CHIAVE_QUI"
    ```
