# Intent & NER NLP System

Aquest projecte implementa un sistema complet de Processament del Llenguatge Natural (PLN) per a dues tasques principals: **classificació d’intencions** i **reconeixement d’entitats anomenades (NER)**, desenvolupat dins l’assignatura *Tractament de la Veu i el Diàleg (TVD)*.

## Contingut del projecte

### 1. Classificació d’intencions

Es desenvolupa un pipeline complet per identificar la intenció d’una frase mitjançant models seqüencials. Inclou:

* Preparació del dataset i tokenització.
* Embeddings amb diverses dimensions.
* Models basats en **Embedding + GlobalMaxPooling**, **CNN**, **RNN (LSTM/GRU/BiLSTM)**.
* Regularització amb Dropout i anàlisi de sobreajust.
* Estratègies de balanceig de classes (class weights i oversampling).
* Avaluació amb accuracy i F1, incloent anàlisi d’errors.

### 2. Reconeixement d’entitats (NER)

Implementació seqüencial per etiquetar cada token amb el seu tag BIO. Inclou:

* Codificació d’etiquetes, tractament del padding i alineament token-etiqueta.
* CNN per capturar patrons locals.
* Models recurrents bidireccionals (BiLSTM i BiGRU).
* Arquitectures Transformer adaptades a seqüències curtes.
* Regularització i balanceig de classes per millorar entitats minoritàries.
* Avaluació amb **F1 macro**, **F1 ponderada** i mètriques sense padding.

## Models desenvolupats

Els models implementats inclouen:

* Models base seqüencials (Embedding + Dense).
* CNN amb diversos kernels.
* BiLSTM i BiGRU amb múltiples capes.
* Transformer amb atenció multihead i feed-forward profund.
* Versions regularitzades i balancejades per classe.

## Principals resultats

* Classificació d’intencions: millores progressives mitjançant embeddings més grans, CNN optimitzades i regularització, fins a obtenir accuracies superiors al 0.95.
* NER: millora notable en Macro F1 amb CNN + BiGRU i Transformers, assolint models robustos i equilibrats tot i el desbalanceig del dataset.

## Autores

Paula Justo
Júlia Pedrol

Grau en Intel·ligència Artificial — FIB (UPC)
