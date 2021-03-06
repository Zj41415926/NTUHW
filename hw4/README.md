### ETF評比績效理論實作
#### 分析結果
排序出來的資料請見ranking.ipynb，以下的相似程度計算結果也請見ranking.ipynb的最後一部分。相似程度的衡量方式我使用的是逆序比例。例如，['B', 'A', 'C']和['C', 'A', 'B']兩序列中，在集合任取兩個物品，這兩個序列給他們的相對順序有100%的機率是不相同的，也就是此兩序列完全不相似。若是['B', 'A', 'C']和['B', 'C', 'A']，則逆序比例為1/3，比較相似。可以看出此逆序比例這個指標數值越低，代表兩序列越相似。
首先，分析週資料和月資料的結果評比相似程度。三種指標在週資料和月資料兩種排序模式的逆序比例分別(依A,B,C的順序)為5.7%，6.1%，和10.1%，代表週資料和月資料的排序結果其實十分相似，尤其是A指標，相似程度高達95%。
再來分析三種評比指標的結果相似程度。A指標和B指標間的逆序比例，週和月資料取平均後大約為3%而已，也就是相似度高達97%。
但A指標和C指標間的逆序比例，及B指標和C指標間的逆序比例，皆為13%左右，也就是C指標評量的結果和A及B差別較大。

總結而論，A指標(Generalized Sharp Ratio)與B指標(Omega)評比效果相近，而C(Riskness R)則與前二者差異相較明顯，從公式上來說是較可以推測因為Omega指標與Sharp Ratio差別在考慮了更高階的動差，在評估報酬並非常態分佈的商品標的可以突顯其優勢，但若選擇的標的報酬率分配都接近常態，則二者所評比的績效差異便較不明顯。
