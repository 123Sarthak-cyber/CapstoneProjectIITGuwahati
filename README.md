# CapstoneProjectIITGuwahati
Tech stacks used
Core Technologies
Python - Primary programming language
Pandas - Data manipulation and analysis
NumPy - Numerical computations
Pathway - Real-time data processing framework
Bokeh - Interactive data visualization

Supporting Libraries
datetime - Time handling
math - Mathematical operations (Haversine distance)
scipy (potential extension) - For more advanced mathematical models

Architecture Flow Diagram
┌───────────────────────────────────────────────────────────────────────────────┐
│                                                                               │
│                    DYNAMIC PARKING PRICING SYSTEM ARCHITECTURE                │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌───────────────────────────────────────────────────────────────────────────────┐
│                                                                               │
│                             DATA INGESTION LAYER                              │
│                                                                               │
│  ┌─────────────┐    ┌─────────────┐    ┌────────────────┐    ┌─────────────┐  │
│  │   CSV File  │───▶│  Pandas     │───▶│ Data Cleaning  │───▶│ Pathway     │  │
│  │ (dataset.csv)│   │ DataFrame   │    │ & Preprocessing│    │ Table       │  │
│  └─────────────┘    └─────────────┘    └────────────────┘    └─────────────┘  │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌───────────────────────────────────────────────────────────────────────────────┐
│                                                                               │
│                           PRICING MODELS LAYER                                │
│                                                                               │
│  ┌──────────────────────┐    ┌──────────────────────┐    ┌──────────────────┐ │
│  │  Linear Pricing      │    │  Demand-Based        │    │ Competitive      │ │
│  │  Model               │    │  Pricing Model       │    │ Pricing Model    │ │
│  │                      │    │                      │    │                  │ │
│  │ - Simple occupancy   │    │ - Multi-factor       │    │ - Competitor     │ │
│  │   based pricing      │    │   demand function    │    │   analysis       │ │
│  │ - α parameter        │    │ - Smoothing          │    │ - Geographic     │ │
│  └──────────┬───────────┘    └──────────┬───────────┘    │   proximity     │ │
│             │                           │                │ - Real-time     │ │
│             └─────────────┬─────────────┘                │   adjustments   │ │
│                           │                              └────────┬─────────┘ │
│                           ▼                                       │           │
│                      ┌───────────┐                                │           │
│                      │ Price     │                                │           │
│                      │ Aggregator│◀───────────────────────────────┘           │
│                      └───────────┘                                            │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌───────────────────────────────────────────────────────────────────────────────┐
│                                                                               │
│                         VISUALIZATION & OUTPUT LAYER                          │
│                                                                               │
│  ┌─────────────┐    ┌─────────────┐    ┌────────────────┐    ┌─────────────┐  │
│  │ Pathway     │───▶│ Bokeh       │───▶│ Interactive    │───▶│ Model       │  │
│  │ Results     │    │ Visualization│    │ Dashboard      │    │ Comparison  │  │
│  └─────────────┘    └─────────────┘    └────────────────┘    └─────────────┘  │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
