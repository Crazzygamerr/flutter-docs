---
layout: post
title: Step area Chart in Flutter Cartesian Charts widget | Syncfusion 
description: Learn here all about step area chart of Syncfusion Flutter Cartesian Charts (SfCartesianChart) widget and more.
platform: flutter
control: Chart
documentation: ug
---

# Step area Chart in Flutter Cartesian Charts (SfCartesianChart)

To render a spline area chart, create an instance of `StepAreaSeries`, and add it to the [`series`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/SfCartesianChart/series.html) collection property of [`SfCartesianChart`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/SfCartesianChart/SfCartesianChart.html). The following properties can be used to customize the appearance of spline area chart.

* [`color`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/CartesianSeries/color.html) - changes the color of the series.
* [`opacity`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/CartesianSeries/opacity.html) - controls the transparency of the chart series.
* [`width`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/CartesianSeries/width.html) - changes the stroke width of the series.

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    child: SfCartesianChart(
                        primaryXAxis: DateTimeAxis(),
                        series: <ChartSeries>[
                            StepAreaSeries<ChartData, DateTime>(
                                dataSource: chartData,
                                xValueMapper: (ChartData data, _) => data.x,
                                yValueMapper: (ChartData data, _) => data.y
                            ),
                            StepAreaSeries<ChartData, DateTime>(
                                dataSource: chartData1,
                                xValueMapper: (ChartData data, _) => data.x,
                                yValueMapper: (ChartData data, _) => data.y
                            )
                        ]
                    )
                )
            )
        );
    }

{% endhighlight %}

![Step area chart](cartesian-chart-types-images/step_area.png)

## Dashed step area

The [`dashArray`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/CartesianSeries/dashArray.html) property of the [`StepAreaSeries`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/StepAreaSeries-class.html) is used to render spline area series with dashes. Odd value is considered as rendering size and even value is considered as gap.

{% highlight dart %} 
    
    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    child: SfCartesianChart(
                        primaryXAxis: DateTimeAxis(),
                        series: <ChartSeries>[
                            StepAreaSeries<ChartData, DateTime>(
                                dataSource: chartData,
                                dashArray: <double>[5, 5],
                                xValueMapper: (ChartData data, _) => data.x,
                                yValueMapper: (ChartData data, _) => data.y
                            )
                        ]
                    )
                )
            )
        );
    }

{% endhighlight %}

![Dashed step area chart](cartesian-chart-types-images/step_area_dashed.png)

#### See Also

* [Color palette](./series-customization#color-palette) 
* [Color mapping](./series-customization#color-mapping-for-data-points)
* [Animation](./series-customization#animation)
* [Gradient](./series-customization#gradient-fill)
* [Empty points](./series-customization#empty-points)  
* [Sorting](./series-customization##sorting) 