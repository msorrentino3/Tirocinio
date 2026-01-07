# Tirocinio
Questo progetto implementa un sistema di Intrusion Detection basato su architettura multi-agente, che combina:
Machine Learning (DistilBERT)
Analisi statistica
Memoria contestuale
Policy adattiva

Il sistema è in grado di classificare log di rete come attacco o traffico normale e di decidere automaticamente azioni di sicurezza

# Contenuto del progetto
AiAgentMultiArchitetture.py → script principale

data.csv → dataset di addestramento

README.md → guida all’uso

# Requisiti di sistema
Python 3.8 o superiore

Sistema operativo: Windows / macOS / Linux

(Opzionale ma consigliato) GPU CUDA per accelerare l’addestramento

# Clonare o scaricare il repository
Opzione consigliata (Git):

git clone https://github.com/msorrentino3/Tirocinio/blob/main/AiAgentMultiArchitetture.py

cd NOME_REPOSITORY

Oppure:

Code → Download ZIP

Estrai la cartella

Creare un ambiente virtuale (consigliato)
macOS / Linux

python -m venv venv

source venv/bin/activate

Windows

python -m venv venv

venv\Scripts\activate

# Nota su PyTorch
Per usare la GPU, installa PyTorch seguendo le istruzioni ufficiali: https://pytorch.org/get-started/locally/

# Dataset

Il file data.csv deve essere presente nella stessa cartella dello script.

Se si vuole usare usare un proprio dataset assicuratevi che sia strutturato nel seguente formato:

Scr_IP

Des_IP

Protocol

Service

OSSEC_alert

class3 (valori:1 (Attack) / 0 (Normal)

Il codice genera automaticamente:

la colonna label (1 = attacco, 0 = normale)

la colonna text usata per addestrare DistilBER

Per avviare addestramento + valutazione + simulazione multi-agente:

# Esecuzione del codice

python AiAgentMultiArchitetture.py


Il codice esegue automaticamente:

Caricamento del dataset

Addestramento del modello DistilBERT

Valutazione con:

Accuracy

Precision

Recall

F1-score

Avvio del sistema multi-agente

Simulazione di log di rete

# Output atteso

Durante l’esecuzione vedrai:

perdita media per epoca

metriche finali di classificazione

decisioni del sistema IDS

# Architettura Multi-Agent

Il sistema è composto dai seguenti agenti:

LogAgent → osserva i log

DetectionAgent → classificazione ML (DistilBERT)

StatisticalAgent → rileva pattern anomali nel tempo

ContextAgent → usa la memoria storica per IP

FusionAgent → combina le decisioni

PolicyAgent → decide l’azione di sicurezza

ResponseAgent → esegue l’azione

LearningAgent → adatta la soglia nel tempo










