# Funnel

### Sample

![Sample Funnel Chart](images/funnel.png)

The following property values create the sample chart pictured above.

**Title**

```javascript
{
    text: "Test Title 1",
    ...
}
```

**Subtitle**

```javascript
{
    text: "",
    ...
}
```

**Legend**

```javascript
{
	enabled: true,
    source: "labels",
    ...
}
```

**Options**

```javascript
Table(
    { key: "funnel.mode", value: "ladder" }
)
```

**Data**

```javascript
{
    labels: ["Label 1","Label 2","Label 3","Label 4","Label 5","Label 6","Label 7"],
    table: Table(
        { key:"values", values: [520, 200, 380, 400,510, 650, 710] }
    )
}
```

### All Options

| Key                     | Remark                                                       |
| ----------------------- | ------------------------------------------------------------ |
| funnel.mode             | The funnel chart has 3 modes: **ladder**, **rectangle** and **pyramid**. The default value is `ladder`.<br />`ladder`<br />![Funnel Chart in Ladder Mode](images/funnel-ladder.png)<br />`rectangle`<br />![Funnel Chart in Rectangle Mode](images/funnel-rectangle.png)<br />`pyramid`<br />![Funnel Chart in Pyramid Mode](images/funnel-pyramid.png)<br />In pyramid mode, the area (**not height**) of parts are calculated from input values. |
| funnel.sort             | You can sort input values. The direction can be **none**, **ascending** and **descending**. The default value is `none`.<br />For example, sorting in descending direction looks like this:<br />![Funnel Chart in Descending Mode](images/funnel-descending.png) |
| funnel.orientation      | You can display the chart in different orientations, **vertical** and **horizontal**. The default value is `vertical`.<br /> Horizontal mode looks like this:<br />![Funnel Chart in Horizontal Mode](images/funnel-horizontal.png) |
| funnel.align            | You can also align all bars to one side. In horizontal mode, you can use **top**, **middle** and **bottom**. In vertical mode, you can use **left**, **center** and **right**. The default value is `center`.<br />  For example, align to the left looks like this:<br />![Funnel Chart in Left Mode](images/funnel-left.png) |
| funnel.maxBarLength     | You can change the max bar length of the chart. Can be **0~1**. The default value is `1`. |
| funnel.itemGap          | You can change gap between two bars. The default value is `10`. |
| funnel.connectorColor   | You can change the color of the gap. The default value is data color. |
| funnel.connectorOpacity | You can also change the opacity of the gap fill. The default value is `0.3`. |

#### Label Options

A funnel chart can display up to 3 labels. When all 3 labels are enabled, it looks like this:

![Funnel Labels](images/funnel-labels.png)

From left to right they are: **labels**, **value labels**, and **percentage labels**.

| Key                                                          | Remark                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| funnel.labels<br />funnel.labels.value<br />funnel.labels.percentage | Should the chart display labels or not? Can be **true** or **false**. The default value is `false`. |
| funnel.labels.value.dx<br />funnel.labels.percentage.dx      | X Offset of labels.                                          |
| funnel.labels.value.dy<br />funnel.labels.percentage.dy      | X Offset of labels.                                          |
| funnel.labels.percentage.mode                                | How to calculate the percentage value.<br />Available values:<br />`sum`: value / sum of all values<br />`max`: value / max value<br />`last`: value / value of last data. |
| funnel.labels.align                                          | Alignment of the labels. Can be **left**, **center** and **right**. The default value is `center`. |
| funnel.labels.verticalAlign                                  | Vertical Alignment of the labels. Can be **top**, **middle** and **bottom**. The default value is `middle`. |
| funnel.labels.fontSize<br />funnel.labels.value.fontSize<br />funnel.labels.percentage.fontSize | Font size of labels.                                         |
| funnel.labels.fontFamily<br />funnel.labels.value.fontFamily<br />funnel.labels.percentage.fontFamily | Font family of labels.                                       |
| funnel.labels.fontWeight<br />funnel.labels.value.fontWeight<br />funnel.labels.percentage.fontWeight | Font weight of labels, can be CSS font weight values.        |
| funnel.labels.fontStyle<br />funnel.labels.value.fontStyle<br />funnel.labels.percentage.fontStyle | Font style of labels, can be CSS font style values.          |
| funnel.labels.color<br />funnel.labels.value.color<br />funnel.labels.percentage.color | Color of labels. The default value is `#ffffff`.             |
| funnel.labels.additionalStyles<br />funnel.labels.value.additionalStyles<br />funnel.labels.percentage.additionalStyles | You can add other CSS style rules here.                      |


