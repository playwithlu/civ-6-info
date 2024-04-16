# Great Scientist (Civ5)

Game Info.
A [Great%20People%20%28Civ5%29](Great Person), specialized in science research.
The unit is expended after performing either of these actions.
Strategy.
In [vanilla](vanilla) "[Civilization%20V](Civilization V)", the Great Scientist can use Discover Technology to grant you a free [List%20of%20technologies%20in%20Civ5](technology). In ' and ', this ability is replaced by the Boost Science ability, which lets you immediately gain an amount of based on the output of your [Civilizations%20%28Civ5%29](civilization). It is usually enough to finish researching the current technology, and even boost another one! Use this if you need an immediate result.
Note that you can use Boost Science from anywhere; you don't need to move the Scientist anywhere specifically.
Alternatively, the Great Scientist can construct an [Academy%20%28Civ5%29](Academy) for a long-term boost in a [City%20%28Civ5%29](city). In the early game, constructing Academies is recommended, as the long-term gains will surpass the instant gain of Boost Science. Later in the game, Boost Science may be worth many tens of turns' worth of Academy . Since you can see how much Boost Science is worth by mousing over the button, you can judge its worth based on how many turns you expect are left in the game (or until you get enough tech to go for your desired [Victory%20%28Civ5%29](victory)). Since the Academy affects the output of an individual city, its gains are augmented by all scientific buildings with a percentage bonus, like the [Research%20Lab%20%28Civ5%29](Research Lab).
Formula.
The number of science beakers yielded by the Boost Science ability is dependent on both your empire's past output and your [Speed%20%28Civ5%29](game speed) setting. It is calculated as follows:
In the XML files this value is actually defined as
 (Science income) * &lt;BaseBeakersTurnsToCount&gt; * &lt;ResearchPercent&gt; / 100
where BaseBeakersTurnsToCount is defined under &lt;Units&gt;&lt;Type&gt;UNIT_SCIENTIST&lt;/Type&gt;&lt;/Units&gt;
and ResearchPercent is defined under &lt;GameSpeeds&gt;&lt;Type&gt;GAMESPEED_MARATHON&lt;/Type&gt;&lt;/GameSpeeds&gt;, &lt;GameSpeeds&gt;&lt;Type&gt;GAMESPEED_EPIC&lt;/Type&gt;&lt;/GameSpeeds&gt;, &lt;GameSpeeds&gt;&lt;Type&gt;GAMESPEED_STANDARD&lt;/Type&gt;&lt;/GameSpeeds&gt;, and &lt;GameSpeeds&gt;&lt;Type&gt;GAMESPEED_QUICK&lt;/Type&gt;&lt;/GameSpeeds&gt;.
The default value of BaseBeakersTurnsToCount is 8, while the default value of ResearchPercent is 67 for Quick, 100 for Standard, 150 for Epic and 300 for Marathon.
It should be noted that the output of Boost Science varies wildly in the first 8 turns. During this time the game sets BaseBeakersTurnsToCount = 3 on Turn 0, then BaseBeakersTurnsToCount = 4 on Turn 1, then BaseBeakersTurnsToCount = 5 on Turn 2, and so on until the turn number is equal to the value of BaseBeakersTurnsToCount set in the XML files. At this point, it will begin using the correct BaseBeakersTurnsToCount value. This appears to be a testing mechanic that was not removed from the game on release, due to the fact that it is impossible to acquire a Great Scientist prior to Turn 8 in an unmodded game. If you are modding the game or creating a [List%20of%20scenarios%20in%20Civ5](scenario), make sure that you do not give players access to a Great Scientist in the first 8 turns of the game.
Also, if you make a mod that significantly increases the ResearchPercent value but not the rest of the gamespeed values, you should decrease the BaseBeakersTurnsToCount value to avoid Boost Science becoming overpowered.
Setting BaseBeakersTurnsToCount = 0 will remove the Boost Science ability entirely from the unit.