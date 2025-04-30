
```mermaid
flowchart TD
    %% 标题（模拟标题框）
    Title[简要判定逻辑] --> A

    %% 输入条件（左侧，绿色）
    A[输入条件<br>- 武器类型 (轻武器/重武器)<br>- 地形 (铺装路面/沙滩/丘陵/山地)<br>- 天气 (晴朗/雨天/雾天/霾天)<br>- 昼夜 (白天/夜晚)<br>- 毁伤部位 (轻武器：头部/胸部等；重武器：炮塔/履带等)] --> B

    %% 判定流程（中间部分）
    subgraph 判定流程
        %% 基础速度计算（绿色）
        B[基础速度计算<br>- 轻武器：根据地形+昼夜确定<br>- 重武器：根据最高速度+地形确定] --> C

        %% 系数计算（蓝色）
        C[系数计算<br>- 地形系数<br>- 天气系数<br>- 昼夜系数<br>- 毁伤系数] --> D

        %% 综合计算（红色）
        D[综合计算<br>实际速度 = 基础速度 × 各系数]
    end

    %% 输出（右侧，蓝色）
    D --> E[输出<br>实际机动速度 (km/h)]

    %% 样式定义（设置颜色）
    style Title fill:#FF0000,stroke:#000000,color:#FFFFFF
    style A fill:#00FF00,stroke:#000000
    style B fill:#00FF00,stroke:#000000
    style C fill:#0000FF,stroke:#000000,color:#FFFFFF
    style D fill:#FF0000,stroke:#000000,color:#FFFFFF
    style E fill:#0000FF,stroke:#000000,color:#FFFFFF
