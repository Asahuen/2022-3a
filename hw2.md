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
```
    
### Graphviz
![pert](https://github.com/Asahuen/2022-3a/blob/main/%E7%B3%BB%E7%B5%B1%E5%88%86%E6%9E%90pert_diagram.jpg)

```graphviz
digraph {
    node[shape=record];
    rankdir="LR";
    no1 [label = "研礙計劃 | 編號:1 | 開始:第1天 | 結束:第1天 | 需時:1天"]
    no2 [label = "任務分配 | 編號:2 | 開始:第2天 | 結束:第5天 | 需時:4天"]
    no3 [label = "取得硬體 | 編號:3 | 開始:第2天 | 結束:第18天 | 需時:17天"]
    {rank=same;no2 no3}
    no1->no2
    no1->no3
    no4 [label = "程式開發 | 編號:4 | 開始:第6天 | 結束:第76天 | 需時:70天"]
    no2->no4
    no5 [label = "安裝硬體 | 編號:5 | 開始:第19天 | 結束:第29天 | 需時:10天"]
    no3->no5
    no6 [label = "程式測試 | 編號:6 | 開始:第77天 | 結束:第107天 | 需時:30天"]
    no4->no6
    no7 [label = "撰寫使用手冊 | 編號:7 | 開始:第30天 | 結束:第55天 | 需時:25天"]
    no8 [label = "轉換檔案 | 編號:8 | 開始:第30天 | 結束:第50天 | 需時:20天"]
    {rank=same;no7 no8}
    no5->no7
    no5->no8
    no9 [label = "系統測試 | 編號:9 | 開始:第108天 | 結束:第133天 | 需時:25天"]
    no6->no9
    no10 [label = "使用者訓練 | 編號:10 | 開始:第56天 | 結束:第76天 | 需時:20天"]
    no7->no10
    no8->no10
    no11 [label = "使用者測試 | 編號:11 | 開始:第134天 | 結束:第159天 | 需時:25天"]
    no10->no11
    no9->no11
}
```

### Critical Path 
關鍵路徑： 1 → 2 → 4 → 6 → 9 → 11
