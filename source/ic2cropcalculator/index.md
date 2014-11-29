---
title: IC2 Crop Calculator
---

## 概要

IndustrialCraft2 の農業要素である品種改良についての計算機です。
各品種を親とした時、目的の品種に突然変異する確率をそれぞれ算出します。
*複数の品種を親としたときは平均になります。*
[IndustrialCraft2ソースコード木パイプ](http://www54.atwiki.jp/mi_ic2/)
及び IndustrialCraft2 experimental ビルド 301 のバイナリを参考に作成しています。
*今現在、 experimental 版と lf 版の農業要素にほぼ差はありません。*

## 注意

突然変異先の環境が成長可能な環境か、による候補へ含めるかどうかの計算を
無視しているため、結果はあくまで**相対的な目安である。**
*すなわち、目的の品種以外が成長できない環境を用意すれば、
計算結果よりも高い確率で目的の品種へ突然変異が行える。*

[IndustrialCraft2ソースコード木パイプ](http://www54.atwiki.jp/mi_ic2/)
で言及されているバグについても現状に沿うためにバグ通りの計算方法を採用しているが、
修正された際、計算結果が修正後の実際と異なる可能性がある。

<section id="input">
    <h2>入力欄</h2>
    <form>
        <label for="target">目的の品種
            <select name="target" id="target"></select>
        </label>
        <label for="gregtech">
            <input type="checkbox" name="addon" value="gregtech" id="gregtech">
            GregTech
        </label>
    </form>
</section>

<section id="result">
    <h2>計算結果</h2>
    <table>
        <thead>
            <tr><th>作物</th><th>確率</th></tr>
        </thead>
        <tbody>
        </tbody>
    </table>
</section>

<script src="//code.jquery.com/jquery-2.0.3.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.5.2/underscore-min.js"></script>
<script src="/javascripts/ic2cropcalculator.js"></script>
