### Mermaid
```mermaid
gantt
    title 任務清單

    section 任務
    研礙計劃           :a1, 2022-09-01, 1d
    任務分配           :a2, after a1  , 4d
    取得硬體           :a3, after a1  , 17d
    程式開發           :a4, after a2  , 70d
    安裝硬體           :a5, after a3  , 10d
    程式測試           :a6, after a4  , 30d
    撰寫使用手冊        :a7, after a5  , 25d
    轉換檔案           :a8, after a5  , 20d
    系統測試           :a9, after a6  , 25d
    使用者訓練         :a10, after a7  , 20d
    使用者測試         :a11, after a9  , 25d
    
    digraph {
	node[shape=record];
	rankdir="LR";
    no1 [label = "研礙計劃 | 編號:1 | 開始:第1天 | 結束:第10天 | 需時:10天"]
    no2 [label = "任務分配 | 編號:2 | 開始:第4天 | 結束:40 | 需時:30天"]
    no1->no2
    no3 [label = "取得硬體 | 編號:3 | 開始:第41天 | 結束:第45天 | 需時:5天"]
    no4 [label = "程式開發 | 編號:4 | 開始:第41天 | 結束:第65天 | 需時:25天"]
    {rank=same;no3 no4}
    no2->no3
    no2->no4
    no5 [label = "安裝硬體 | 編號:5 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no3->no5
    no4->no5
    no5 [label = "程式測試 | 編號:6 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no5 [label = "撰寫使用手冊 | 編號:7 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no5 [label = "轉換檔案 | 編號:8 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no5 [label = "系統測試 | 編號:9 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no5 [label = "使用者訓練 | 編號:10 | 開始:第66天 | 結束:第95天 | 需時:30天"]
    no5 [label = "使用者測試 | 編號:11 | 開始:第66天 | 結束:第95天 | 需時:30天"]