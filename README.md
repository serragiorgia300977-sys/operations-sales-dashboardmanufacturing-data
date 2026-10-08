# Operations & Sales Executive Dashboard

Un sistema di Business Intelligence e analisi dati dedicato al monitoraggio della performance operativa e commerciale in ambito manifatturiero.

## 📊 Panoramica

Questo progetto fornisce una suite di dashboard esecutive per il tracking in tempo reale di KPI operativi e commerciali. La soluzione integra dati di produzione, vendite e qualità, offrendo visibilità strategica sulla performance aziendale.

## 🎯 Obiettivi Principali

- **Monitoraggio Real-Time**: Tracciamento continuativo di metriche operative e commerciali
- **Executive Storytelling**: Narrativa visuale dei dati per supportare decisioni strategiche
- **Analisi Predittiva**: Identificazione di trend e anomalie nelle performance
- **Ottimizzazione Operativa**: Data-driven insights per migliorare efficienza e margini

## 📈 KPI Tracciati

### Metriche Finanziarie
- **Fatturato Totale**: Sum of Fatturato_Totale
- **Costo Produttivo**: Sum of Cost_Totali
- **Margine Operativo**: Sum of Margine_Totale
- **Margine %**: Average Margin_Pct

### Metriche Operative
- **Lead Time P90**: Tempo di consegna al 90° percentile
- **Tempo di Fermo Macchina**: Sum of Fermi_Totali_min
- **Inattività Media**: Average Inattivita_Media_pct
- **Ordini di Produzione**: Sum of Totale_Ordini

### Metriche di Qualità
- **Tasso Difetti**: Average Avg_Defect_Rate
- **Alert e Anomalie**: Conteggio segnalazioni critiche
- **Status Operativo**: OK vs ALERT (regolarità vs criticità)

## 📅 Periodo di Analisi

- **Range Temporale**: 2/10/2026 - 5/24/2026
- **Granularità**: Giornaliera
- **Ultima Sincronizzazione**: 2026-10-08

## 🔄 Ciclo di Produzione Tipico

Nel periodo analizzato:
- **Fatturato Registrato**: ~3.71M€
- **Regolarità Operativa (OK)**: 83.5%
- **Giorni in Criticità (ALERT)**: 16.5%

Le giornate di alert concentrano volumi inferiori e tassi di inattività più elevati rispetto alla media standard.

## 🚨 Azioni Tattiche & Strategiche

### Azioni Tattiche Immediate
- Riduzione dei colli di bottiglia nelle fasi di completamento
- Presidi di manutenzione preventiva per abbassare il Lead Time P90 nei giorni critici

### Azioni Preventive Strategiche
- Pianificazione anticipata di lotti complessi nei giorni ad alto rischio statistico
- Strutturazione di allarmi automatici via email configurati su KPI critici per intervento tempestivo prima dell'erosione del margine

## 📁 Struttura Progetto

```
operations-sales-dashboardmanufacturing-data/
├── README.md                    # Documentazione principale
├── data/
│   ├── raw/                     # Dati grezzi da ERP/MES
│   ├── processed/               # Dati elaborati e aggregati
│   └── dimensions/              # Tabelle dimensionali
├── dashboards/
│   ├── executive-summary/       # Report esecutivo narrativo
│   └── operations-analytics/    # Dashboard analitico dettagliato
├── analytics/
│   ├── kpi-definitions/         # Definizioni metriche
│   ├── sql-queries/             # Query di aggregazione
│   └── ml-models/               # Modelli predittivi (optional)
├── documentation/
│   ├── data-dictionary.md       # Glossario campi
│   ├── etl-process.md           # Flusso di caricamento dati
│   └── alert-thresholds.md      # Soglie di criticità
└── config/
    ├── dashboard-filters.json   # Configurazione filtri
    └── alert-rules.json         # Regole di segnalazione
```

## 🔧 Stack Tecnologico

- **BI Tool**: Microsoft Power BI / Tableau (basato su schermate)
- **Data Source**: ERP/MES aziendale
- **Database**: Data Warehouse (SQL Server / PostgreSQL / Snowflake)
- **Automation**: ETL pipeline (SSIS / Apache Airflow / Talend)
- **Alert System**: Email-based KPI notifications

## 📊 Dashboard Principali

### 1. Executive Summary & Storytelling
Narrativa visuale della performance con:
- KPI headline (Fatturato, Margine, Alert%)
- Context story dei dati (cosa è successo nel periodo)
- Azioni tattiche e strategiche raccomandate
- Filtri date per analisi storiche

### 2. Operations & Sales Executive Dashboard
Dashboard analitica con:
- Metriche di sintesi per linea di prodotto
- Trend temporale di Lead Time e Performance
- Tabella dettagliata transazionale
- Drill-through su anomalie e giorni critici
- Visualizzazioni comparative (OK vs ALERT)

## 🔄 Flusso Dati ETL

```
ERP/MES System
    ↓
[Raw Data Layer] → daily extraction
    ↓
[Transform & Aggregate] → SQL/Python processing
    ↓
[Data Warehouse] → dimensional model
    ↓
[BI Dashboard] → Power BI / Tableau refresh
    ↓
[Alert Engine] → KPI monitoring & notifications
```

## ⚙️ Configurazione & Filtri

I dashboard supportano:
- **Filtri Temporali**: Range date, granularità (giorno/settimana/mese)
- **Filtri Operativi**: Status (OK/ALERT), linea di produzione, categoria prodotto
- **Filtri Analitici**: Margine range, Lead Time threshold, Defect Rate limit

## 📧 Notifiche Automatiche

Sistema di alert configurato per:
- Lead Time P90 superiore a soglia configurata
- Tasso difetti superiore a 2.5%
- Giorni con inattività media > 15%
- Comunicazione via email su KPI critici

## 🚀 Getting Started

1. **Accesso ai Dati**: Connettersi all'ERP/MES aziendale
2. **Refresh Dashboard**: Caricamento automatico giornaliero o manuale
3. **Interpretazione KPI**: Consultare data dictionary per definizioni esatte
4. **Azioni Correttive**: Seguire le raccomandazioni tattiche/strategiche

## 📚 Documentazione Aggiuntiva

- [Data Dictionary](./documentation/data-dictionary.md) - Glossario campi e metriche
- [ETL Process](./documentation/etl-process.md) - Descrizione del flusso di caricamento
- [Alert Thresholds](./documentation/alert-thresholds.md) - Soglie critiche e regole
- [KPI Definitions](./analytics/kpi-definitions/) - Formule e metodologie di calcolo

## 👥 Contatti & Supporto

Per domande o segnalazioni:
- Dashboard Support: [email / team]
- Data Governance: [team responsabile]
- Alert Administration: [team tecnico]

## 📄 Licenza

[Specificare licenza - es. Internal Use Only, MIT, Apache 2.0]

---

**Ultimo Aggiornamento**: Ottobre 2026  
**Stato**: Active Development
