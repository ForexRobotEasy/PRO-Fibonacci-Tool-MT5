README file for the code - PRO Fibonacci Tool MT5

This code is a custom Fibonacci tool developed for MetaTrader 5 (MT5) platform. The tool allows traders to draw Fibonacci retracement and expansion levels on their charts, edit existing levels, and remove levels as needed. It provides a convenient way for traders to analyze price movements and identify potential support and resistance levels.

To use this tool, you need to include the necessary libraries: Trade.mqh, ChartObjectsFibo.mqh, and HotKeys.mqh. These libraries provide the required functions and objects for trading, chart objects, and hotkeys respectively.

The code defines a constant MAX_LEVELS which represents the maximum number of Fibonacci levels that can be drawn. The value of MAX_LEVELS is set to 10, but you can modify it according to your requirements.

The code also defines a global variable `trade` of type CTrade, which is the trade object used for executing trading operations.

Next, there is a class CFibonacciTool which encapsulates the functionality of the Fibonacci tool. It has a private member variable `fiboLevels` which is an array of CChartObjectFibo objects used to store the Fibonacci levels. It also has a private member variable `currentLevel` which keeps track of the current number of Fibonacci levels drawn.

The CFibonacciTool class has several member functions:

1. `DrawLevels()`: This function is used to draw Fibonacci retracement and expansion levels on the chart. It calculates the price range and time range of the chart and then calculates the Fibonacci levels based on these ranges. It creates a new CChartObjectFibo object with the calculated levels, sets the color of the object to red, and redraws it on the chart.

2. `EditLevel(int levelIndex, double newLevel)`: This function allows you to edit a specific Fibonacci level. It takes the index of the level to be edited and the new level value as parameters. If the level index is valid, it updates the level value and redraws the level on the chart.

3. `RemoveLevel(int levelIndex)`: This function allows you to remove a specific Fibonacci level. It takes the index of the level to be removed as a parameter. If the level index is valid, it deletes the level object and updates the array of Fibonacci levels.

The code also includes an initialization function `OnInit()` and a deinitialization function `OnDeinit()`. The `OnInit()` function enables hotkeys for drawing Fibonacci levels and initializes the trade object. The `OnDeinit()` function is called when the program is stopped or the chart is closed. It removes all Fibonacci levels created by the tool.

In addition to the above functions, the code includes three custom functions: `DrawLevels()`, `EditLevel(int levelIndex, double newLevel)`, and `RemoveLevel(int levelIndex)`. These functions are used as event handlers for the hotkeys defined in the `OnInit()` function. They simply call the corresponding functions of the CFibonacciTool object.

Please note that Forex Robot Easy is not the official developer of this product. We only provide sample code that demonstrates the functionality of this product. To find the official developer of this product, please refer to the link provided in the header section.

For detailed reviews and trading results of this product, please visit the following link: [PRO Fibonacci Tool MT5 Review](https://forexroboteasy.com/forex-robot-review/pro-fibonacci-tool-mt5-review-unique-forex-software-for-traders/).
