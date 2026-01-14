# FI Surveillance Transition Flow

``` mermaid
flowchart TD

A["Start<br/>STS Generates All FI Surveillance Alerts"]
B["Interim 1 (Jan)<br/>- Trading Hub onboards all FI except Nova/Murex<br/>- Trading Hub generates Spoofing & Insider alerts for non-Nova/Murex FI"]
C["Duplicate Alerts<br/>Both STS & Trading Hub for non-Nova/Murex FI"]
D["Spoofing & Insider Trading cannot be turned off in STS<br/>(Nova/Murex alerts still required)"]
E["FI feeds cannot be turned off in STS<br/>(Other FI scenarios e.g. wash trading, ramping etc still required)"]
F["STS interim handling<br/>- Marks non-Nova/Murex Spoofing/Insider Trading alerts inactive<br/>- Only Nova/Murex Spoofing/Insider Trading FI alerts active in STS"]
G["Interim 2<br/>- Nova/Murex FI Onboarded into SDML<br/>- Trading Hub covers all FI for Spoofing & Insider<br/>- Spoofing & Insider alerts switched off in STS"]
H["Final<br/>- All FI scenarios enabled in Trading Hub<br/>- All FI feeds stopped to STS<br/>- STS decommissioned for FI surveillance"]

A --> B --> C --> D --> E --> F --> G --> H

%% Pastel styling equivalent to PlantUML
style A fill:#B0C4DE,stroke:#333333,rx:10,ry:10
style B fill:#FFFACD,stroke:#333333,rx:10,ry:10
style C fill:#FFFACD,stroke:#333333,rx:10,ry:10
style D fill:#FFFACD,stroke:#333333,rx:10,ry:10
style E fill:#FFFACD,stroke:#333333,rx:10,ry:10
style F fill:#FFE4B5,stroke:#333333,rx:10,ry:10
style G fill:#E6E6FA,stroke:#333333,rx:10,ry:10
style H fill:#90EE90,stroke:#333333,rx:10,ry:10
```
