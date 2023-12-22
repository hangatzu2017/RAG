# Retrieval Augmented Generation (RAG)
Appunti, Test e Tecniche inerenti il sistema di Retrival Augmented Generation applicato ai Large Language Models

## Introduzione
I modelli linguistici di uso generale (General Purpose Language Models) possono svolgere diversi compiti, qualoi ad esempio l'analisi del sentimento ed il riconoscimento di entità. Questi compiti generalmente non richiedono conoscenze di base aggiuntive.

Per compiti più complessi dove la conoscenza profonda dell'argomento è indispensabile, è invece possibile costruire un sistema basato su modelli linguistici che accedano a fonti di conoscenza esterne (knoledge base) per completare i compiti assegnati. Ciò consente una maggiore coerenza fattuale, migliora l'affidabilità delle risposte generate e aiuta a mitigare il problema dell' "allucinazione" tipico degli LLM.

I ricercatori di Meta AI hanno introdotto un metodo chiamato Retrieval Augmented Generation (RAG) per affrontare questo genere di problema. Il RAG combina una componente di recupero delle informazioni con un modello in grado di generare testo. Il RAG può essere messo a punto e le sue basi di conoscenza interne possono essere modificate in modo diretto ed efficiente, senza bisogno di riaddestrare (retrain) l'intero modello.

Il RAG riceve un input e recupera un insieme di documenti pertinenti, dati da una fonte pubblica e/o privata (ad esempio, Wikipedia). I documenti vengono concatenati come contesto con la richiesta originale di input (domanda utente) ed inviati al generatore di testo che produce l'output finale. Questo rende il RAG adattabile a situazioni in cui i fatti possono evolvere nel tempo. Risulta molto utile poichè la conoscenza parametrica degli LLM è statica (ferma alla data dell'ultimo addestramento). Il RAG permette ai modelli linguistici di evitare continui addestramenti, consentendo l'accesso alle informazioni più recenti per generare output affidabili attraverso la generazione basata sul reperimento delle informazioni da fonti certe.

