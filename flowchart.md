# Mobility Model Flowchart

Below is the logic flowchart for the mobility model, used to calculate the actual speed.

```mermaid
flowchart LR
    Title[Logic Flow] --> A
    A[Inputs: Weapon Type (Light/Heavy), Terrain Options, Weather Options, Day/Night, Damage Parts (Head/Tracks)] --> B
    subgraph Process
        B[Base Speed: Light (Terrain+Day/Night), Heavy (Max Speed+Terrain)] --> C
        C[Factors: Terrain, Weather, Day/Night, Damage] --> D
        D[Calculation: Speed = Base Speed x Factors]
    end
    D --> E[Output: Speed (km/h)]
    style Title fill:#FF0000,stroke:#000000,color:#FFFFFF
    style A fill:#00FF00,stroke:#000000
    style B fill:#00FF00,stroke:#000000
    style C fill:#0000FF,stroke:#000000,color:#FFFFFF
    style D fill:#FF0000,stroke:#000000,color:#FFFFFF
    style E fill:#0000FF,stroke:#000000,color:#FFFFFF
