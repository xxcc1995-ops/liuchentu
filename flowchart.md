# 机动模型流程图

以下是机动模型的判定逻辑流程图，用于计算实际机动速度。

```mermaid
flowchart LR
    Title[简要判定逻辑] --> A
    A[输入条件 | 武器类型: 轻/重武器 | 地形: 多种选项 | 天气: 多种选项 | 昼夜: 白天/夜晚 | 毁伤部位: 头部/履带等] --> B
    subgraph 判定流程
        B[基础速度计算 | 轻武器: 地形+昼夜 | 重武器: 最高速度+地形] --> C
        C[系数计算 | 地形系数 | 天气系数 | 昼夜系数 | 毁伤系数] --> D
        D[综合计算 | 实际速度 = 基础速度 x 各系数]
    end
    D --> E[输出 | 实际机动速度 (km/h)]
    style Title fill:#FF0000,stroke:#000000,color:#FFFFFF
    style A fill:#00FF00,stroke:#000000
    style B fill:#00FF00,stroke:#000000
    style C fill:#0000FF,stroke:#000000,color:#FFFFFF
    style D fill:#FF0000,stroke:#000000,color:#FFFFFF
    style E fill:#0000FF,stroke:#000000,color:#FFFFFF
