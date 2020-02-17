### Introduction

#### Regular  C# # 


```C#
Console.WriteLine("Hello World");
```

    Hello World


#### New functions


```C#
display("Hello World");
```


    Hello World


#### Read-Eval-Print Loop


```C#
"Hello World"
```




    Hello World



### Nuget Packages and Namespaces


```C#
#r "nuget:XPlot.Plotly"
using XPlot.Plotly;
```


Installing package XPlot.Plotly.........done!



Failed to add reference to package XPlot.Plotly



<table><thead><tr><th><i>index</i></th><th>value</th></tr></thead><tbody><tr><td>0</td><td>error: Unable to load the service index for source https://api.nuget.org/v3/index.json.</td></tr><tr><td>1</td><td>error:   No such host is known.</td></tr></tbody></table>



```C#
var openSeries = new Graph.Scatter
{
    name = "Open",
    x = new[] {1, 2, 3, 4}, 
    y = new[] {10, 15, 13, 17}
};

var closeSeries = new Graph.Scatter
{
    name = "Close",
    x = new[] { 2,3,4,5 },
    y = new[] { 16, 5, 11, 9 }
};

var chart = Chart.Plot(new[] {openSeries, closeSeries});
chart.WithTitle("Open vs Close");
display(chart);
```


<div id="2737888c-c4fe-4688-98e2-a852981a8555" style="width: 900px; height: 500px;"></div><script type="text/javascript">

var renderPlotly = function() {
    var xplotRequire = requirejs.config({context:'xplot-2.0.0',paths:{plotly:'https://cdn.plot.ly/plotly-1.49.2.min'}});
    xplotRequire(['plotly'], function(Plotly) {

            var data = [{"type":"scatter","x":[1,2,3,4],"y":[10,15,13,17],"name":"Open"},{"type":"scatter","x":[2,3,4,5],"y":[16,5,11,9],"name":"Close"}];
            var layout = {"title":"Open vs Close"};
            Plotly.newPlot('2737888c-c4fe-4688-98e2-a852981a8555', data, layout);
        });
};
if ((typeof(requirejs) !==  typeof(Function)) || (typeof(requirejs.config) !== typeof(Function))) { 
    var script = document.createElement("script"); 
    script.setAttribute("src", "https://cdnjs.cloudflare.com/ajax/libs/require.js/2.3.6/require.min.js"); 
    script.onload = function(){
        renderPlotly();
    };
    document.getElementsByTagName("head")[0].appendChild(script); 
}
else {
    renderPlotly();
}
</script>



```C#
var chart = Chart.Plot(new List<Graph.Box> 
{ 
    new Graph.Box() { y = new int [] { -40, 24, 36, 52, 67, 99, 26, 28, 20 }, name = "Age" }, 
    new Graph.Box() { y = new int [] { 12, 42, 70, 100, 46, 20, 24, 24, 20 }, name = "Annual Income" }, 
    new Graph.Box() { y = new int [] { 0, 30, 100, 50, 60, 80, 75, 75, 20 }, name = "Spending Score" } 
});

var layout = new Layout.Layout() 
{ 
    title="Shopping Mall Customers Data Distribution", 
    showlegend = false 
};
chart.WithLayout(layout);

display(chart);
```


<div id="6153ad0c-0070-47fd-a5bf-e483a05d4b1d" style="width: 900px; height: 500px;"></div><script type="text/javascript">

var renderPlotly = function() {
    var xplotRequire = requirejs.config({context:'xplot-2.0.0',paths:{plotly:'https://cdn.plot.ly/plotly-1.49.2.min'}});
    xplotRequire(['plotly'], function(Plotly) {

            var data = [{"type":"box","y":[-40,24,36,52,67,99,26,28,20],"name":"Age"},{"type":"box","y":[12,42,70,100,46,20,24,24,20],"name":"Annual Income"},{"type":"box","y":[0,30,100,50,60,80,75,75,20],"name":"Spending Score"}];
            var layout = {"title":"Shopping Mall Customers Data Distribution","showlegend":false};
            Plotly.newPlot('6153ad0c-0070-47fd-a5bf-e483a05d4b1d', data, layout);
        });
};
if ((typeof(requirejs) !==  typeof(Function)) || (typeof(requirejs.config) !== typeof(Function))) { 
    var script = document.createElement("script"); 
    script.setAttribute("src", "https://cdnjs.cloudflare.com/ajax/libs/require.js/2.3.6/require.min.js"); 
    script.onload = function(){
        renderPlotly();
    };
    document.getElementsByTagName("head")[0].appendChild(script); 
}
else {
    renderPlotly();
}
</script>


### PocketView API


```C#
var pocketViewTagMethods = typeof(PocketViewTags)
    .GetProperties()
    .Select(m => m.Name);

display(pocketViewTagMethods);
```


<table><thead><tr><th><i>index</i></th><th>value</th></tr></thead><tbody><tr><td>0</td><td>_</td></tr><tr><td>1</td><td>a</td></tr><tr><td>2</td><td>area</td></tr><tr><td>3</td><td>aside</td></tr><tr><td>4</td><td>b</td></tr><tr><td>5</td><td>body</td></tr><tr><td>6</td><td>br</td></tr><tr><td>7</td><td>button</td></tr><tr><td>8</td><td>caption</td></tr><tr><td>9</td><td>center</td></tr><tr><td>10</td><td>code</td></tr><tr><td>11</td><td>colgroup</td></tr><tr><td>12</td><td>dd</td></tr><tr><td>13</td><td>details</td></tr><tr><td>14</td><td>div</td></tr><tr><td>15</td><td>dl</td></tr><tr><td>16</td><td>dt</td></tr><tr><td>17</td><td>em</td></tr><tr><td>18</td><td>figure</td></tr><tr><td>19</td><td>font</td></tr><tr><td>20</td><td>form</td></tr><tr><td>21</td><td>h1</td></tr><tr><td>22</td><td>h2</td></tr><tr><td>23</td><td>h3</td></tr><tr><td>24</td><td>h4</td></tr><tr><td>25</td><td>h5</td></tr><tr><td>26</td><td>h6</td></tr><tr><td>27</td><td>head</td></tr><tr><td>28</td><td>header</td></tr><tr><td>29</td><td>hgroup</td></tr><tr><td>30</td><td>hr</td></tr><tr><td>31</td><td>html</td></tr><tr><td>32</td><td>i</td></tr><tr><td>33</td><td>iframe</td></tr><tr><td>34</td><td>img</td></tr><tr><td>35</td><td>input</td></tr><tr><td>36</td><td>label</td></tr><tr><td>37</td><td>li</td></tr><tr><td>38</td><td>link</td></tr><tr><td>39</td><td>main</td></tr><tr><td>40</td><td>menu</td></tr><tr><td>41</td><td>menuitem</td></tr><tr><td>42</td><td>meta</td></tr><tr><td>43</td><td>meter</td></tr><tr><td>44</td><td>nav</td></tr><tr><td>45</td><td>ol</td></tr><tr><td>46</td><td>optgroup</td></tr><tr><td>47</td><td>option</td></tr><tr><td>48</td><td>p</td></tr><tr><td>49</td><td>pre</td></tr><tr><td>50</td><td>progress</td></tr><tr><td>51</td><td>q</td></tr><tr><td>52</td><td>script</td></tr><tr><td>53</td><td>section</td></tr><tr><td>54</td><td>select</td></tr><tr><td>55</td><td>small</td></tr><tr><td>56</td><td>source</td></tr><tr><td>57</td><td>span</td></tr><tr><td>58</td><td>strike</td></tr><tr><td>59</td><td>style</td></tr><tr><td>60</td><td>strong</td></tr><tr><td>61</td><td>sub</td></tr><tr><td>62</td><td>sup</td></tr><tr><td>63</td><td>svg</td></tr><tr><td>64</td><td>table</td></tr><tr><td>65</td><td>tbody</td></tr><tr><td>66</td><td>td</td></tr><tr><td>67</td><td>textarea</td></tr><tr><td>68</td><td>tfoot</td></tr><tr><td>69</td><td>th</td></tr><tr><td>70</td><td>thead</td></tr><tr><td>71</td><td>title</td></tr><tr><td>72</td><td>tr</td></tr><tr><td>73</td><td>u</td></tr><tr><td>74</td><td>ul</td></tr><tr><td>75</td><td>video</td></tr></tbody></table>



```C#
var pocketView = table[style: "width: 100%"](tr(td[style:"border: 1px solid black"]("Hello!")));

display(pocketView);
```


<table style="width: 100%"><tr><td style="border: 1px solid black">Hello!</td></tr></table>

