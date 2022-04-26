## [ezmoji](https://github.com/arakilian0/ezmoji)
<!-- ![Alt text](/screenshot.jpg "a title") -->
***:zzz: easy html emojis for the web***

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](https://github.com/arakilian0/ezmoji) [![GitHub release](https://img.shields.io/github/release/arakilian0/ezmoji.svg)](https://github.com/arakilian0/ezmoji/releases/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/arakilian0/ezmoji/blob/master/LICENSE) 

[![Alt text](/screenshot.jpg)](https://github.com/arakilian0/ezmoji)

### What is ezmoji?
ezmoji aims to be a consistent API for [Unicode](https://en.wikipedia.org/wiki/Unicode) Emojis. The project sprung from the need of a Web based Emoji API. The requirements didn't include all possible Emojis, however one of the requirements was plug-and-play. At first I was using [emoji-css](https://github.com/afeld/emoji-css/) and that did the job but it wasn't my desired solution.

The reason it wasn't my desired solution is because the emojis are served as images. Whether it be SVG or PNG. The [Unicode Emoji List](https://unicode.org/emoji/charts/full-emoji-list.html) is a great place to start building an Emoji API because 1: it's Internationaly Standard and 2: It's text based.

Some challanges to tackle for ezmoji would be:
- Wrap around the full [Unicode Emoji List](https://unicode.org/emoji/charts/full-emoji-list.html) with some exceptions
- Re-write/shorten/add codenames to follow a consistent set of patterns
- Lightweight, plug-and-play onboarding

### How do you use ezmoji?
At the current state of the project, simply copy-and-paste. There are only 2 files in this repo that work
towards serving Emojis.
- [`ezmoji.js`*(required)*](https://github.com/arakilian0/ezmoji)
Re-writing for use with front-end frameworks. Currently only functional if the `window` object exists. For example Vanilla JS, jQuery etc.
- [`ezmoji.json`*(optional)*](https://github.com/arakilian0/ezmoji)
The list of all available Emojis in ezmoji. You can use this JSON file along with a custom script in a front-end framework like React or Vue to achieve the same as ezmoji.js.

Check out [example.html](https://github.com/arakilian0/ezmoji) to see how you can use ezmoji in your project.
```html
<-- example.html -->

<h1>This is a :smile:!</h1> <!-- output: This is a 😄! -->
<h2>This is :laughing:!</h2> <!-- output: This is 😆! -->
<h3>This is a :blush:!</h3> <!-- output: This is a 😊! -->

<script>
    var ezmoji={};ezmoji.list={smile:{code:":smile:",emoji:"\ud83d\ude04"},laughing:{code:":laughing:",emoji:"\ud83d\ude06"},blush:{code:":blush:",emoji:"\ud83d\ude0a"},smiley:{code:":smiley:",emoji:"\ud83d\ude03"},relaxed:{code:":relaxed:",emoji:"\ud83d\ude0a"},smirk:{code:":smirk:",emoji:"\ud83d\ude0f"},heart_eyes:{code:":heart_eyes:",emoji:"\ud83d\ude0d"},kissing_heart:{code:":kissing_heart:",emoji:"\ud83d\ude18"},kissing_eyes_closed:{code:":kissing_eyes_closed:",emoji:"\ud83d\ude1a"},flushed:{code:":flushed:",emoji:"\ud83d\ude33"},relieved:{code:":relieved:",emoji:"\ud83d\ude0c"},satisfied:{code:":satisfied:",emoji:"\ud83d\ude06"},grin:{code:":grin:",emoji:"\ud83d\ude01"},wink:{code:":wink:",emoji:"\ud83d\ude09"},stuck_out_tongue_winking_eye:{code:":stuck_out_tongue_winking_eye:",emoji:"\ud83d\ude1c"},stuck_out_tongue_closed_eye:{code:":stuck_out_tongue_closed_eye:",emoji:"\ud83d\ude1d"},grinning:{code:":grinning:",emoji:"\ud83d\ude00"},kissing:{code:":kissing:",emoji:"\ud83d\ude17"},kissing_smiling_eyes:{code:":kissing_smiling_eyes:",emoji:"\ud83d\ude19"},stuck_out_tongue:{code:":stuck_out_tongue:",emoji:"\ud83d\ude1b"},sleeping:{code:":sleeping:",emoji:"\ud83d\ude34"},worried:{code:":worried:",emoji:"\ud83d\ude1f"},frowning:{code:":frowning:",emoji:"\ud83d\ude26"},anguished:{code:":anguished:",emoji:"\ud83d\ude27"},open_mouth:{code:":open_mouth:",emoji:"\ud83d\ude2e"},grimacing:{code:":grimacing:",emoji:"\ud83d\ude2c"},confused:{code:":confused:",emoji:"\ud83d\ude15"},hushed:{code:":hushed:",emoji:"\ud83d\ude2f"},expressionless:{code:":expressionless:",emoji:"\ud83d\ude11"},unamused:{code:":unamused:",emoji:"\ud83d\ude12"},sweat_smile:{code:":sweat_smile:",emoji:"\ud83d\ude05"},sweat:{code:":sweat:",emoji:"\ud83d\ude13"},disappionted_relieved:{code:":disappionted_relieved:",emoji:"\ud83d\ude25"},weary:{code:":weary:",emoji:"\ud83d\ude29"},pensive:{code:":pensive:",emoji:"\ud83d\ude14"},disappionted:{code:":disappionted:",emoji:"\ud83d\ude1e"},confounded:{code:":confounded:",emoji:"\ud83d\ude16"},fearful:{code:":fearful:",emoji:"\ud83d\ude28"},cold_sweat:{code:":cold_sweat:",emoji:"\ud83d\ude30"},persevere:{code:":persevere:",emoji:"\ud83d\ude23"},cry:{code:":cry:",emoji:"\ud83d\ude22"},sob:{code:":sob:",emoji:"\ud83d\ude2d"},joy:{code:":joy:",emoji:"\ud83d\ude02"},astonished:{code:":astonished:",emoji:"\ud83d\ude32"},scream:{code:":scream:",emoji:"\ud83d\ude31"},tired_face:{code:":tired_face:",emoji:"\ud83d\ude2b"},angry:{code:":angry:",emoji:"\ud83d\ude20"},rage:{code:":rage:",emoji:"\ud83d\ude21"},triumph:{code:":triumph:",emoji:"\ud83d\ude24"},sleepy:{code:":sleepy:",emoji:"\ud83d\ude2a"},yum:{code:":yum:",emoji:"\ud83d\ude0b"},mask:{code:":mask:",emoji:"\ud83d\ude37"},sunglasses:{code:":sunglasses:",emoji:"\ud83d\ude0e"},dizzy_face:{code:":dizzy_face:",emoji:"\ud83d\ude35"},imp:{code:":imp:",emoji:"\ud83d\udc7f"},smiling_imp:{code:":smiling_imp:",emoji:"\ud83d\ude08"},neutral_face:{code:":neutral_face:",emoji:"\ud83d\ude10"},no_mouth:{code:":no_mouth:",emoji:"\ud83d\ude36"},innocent:{code:":innocent:",emoji:"\ud83d\ude07"},alien:{code:":alien:",emoji:"\ud83d\udc7d"},yellow_heart:{code:":yellow_heart:",emoji:"\ud83d\udc9b"},blue_heart:{code:":blue_heart:",emoji:"\ud83d\udc99"},purple_heart:{code:":purple_heart:",emoji:"\ud83d\udc9c"},heart:{code:":heart:",emoji:"\u2764\ufe0f"},green_heart:{code:":green_heart:",emoji:"\ud83d\udc9a"},broken_heart:{code:":broken_heart:",emoji:"\ud83d\udc94"},heartbeat:{code:":heartbeat:",emoji:"\ud83d\udc93"},heartpulse:{code:":heartpulse:",emoji:"\ud83d\udc97"},two_hearts:{code:":two_hearts:",emoji:"\ud83d\udc95"},revolving_hearts:{code:":revolving_hearts:",emoji:"\ud83d\udc9e"},cupid:{code:":cupid:",emoji:"\ud83d\udc98"},sparkling_heart:{code:":sparkling_heart:",emoji:"\ud83d\udc96"},sparkles:{code:":sparkles:",emoji:"\u2728"},star:{code:":star:",emoji:"\u2b50\ufe0f"},star2:{code:":star2:",emoji:"\ud83c\udf1f"},dizzy:{code:":dizzy:",emoji:"\ud83d\udcab"},boom:{code:":boom:",emoji:"\ud83d\udca5"},collision:{code:":collision:",emoji:"\ud83d\udca5"},anger:{code:":anger:",emoji:"\ud83d\udca2"},exclamation:{code:":exclamation:",emoji:"\u2757\ufe0f"},question:{code:":question:",emoji:"\u2753"},grey_exclamation:{code:":grey_exclamation:",emoji:"\u2755"},grey_question:{code:":grey_question:",emoji:"\u2754"},zzz:{code:":zzz:",emoji:"\ud83d\udca4"},dash:{code:":dash:",emoji:"\ud83d\udca8"},sweat_drops:{code:":sweat_drops:",emoji:"\ud83d\udca6"},notes:{code:":notes:",emoji:"\ud83c\udfb6"},musical_note:{code:":musical_note:",emoji:"\ud83c\udfb5"},fire:{code:":fire:",emoji:"\ud83d\udd25"},hankey:{code:":hankey:",emoji:"\ud83d\udca9"},poop:{code:":poop:",emoji:"\ud83d\udca9"},shit:{code:":shit:",emoji:"\ud83d\udca9"},plusone:{code:":+1:",emoji:"\ud83d\udc4d"},thumbsup:{code:":thumbsup:",emoji:"\ud83d\udc4d"},minusone:{code:":-1:",emoji:"\ud83d\udc4e"},thumbsdown:{code:":thumbsdown:",emoji:"\ud83d\udc4e"},ok_hand:{code:":ok_hand:",emoji:"\ud83d\udc4c"},punch:{code:":punch:",emoji:"\ud83d\udc4a"},facepunch:{code:":facepunch:",emoji:"\ud83d\udc4a"},fist:{code:":fist:",emoji:"\u270a"},v:{code:":v:",emoji:"\u270c\ufe0f"},wave:{code:":wave:",emoji:"\ud83d\udc4b"},hand:{code:":hand:",emoji:"\u270b"},raised_hand:{code:":raised_hand:",emoji:"\u270b"},open_hands:{code:":open_hands:",emoji:"\ud83d\udc50"},point_up:{code:":point_up:",emoji:"\u261d\ufe0f"},point_down:{code:":point_down:",emoji:"\ud83d\udc47"},point_left:{code:":point_left:",emoji:"\ud83d\udc48"},point_right:{code:":point_right:",emoji:"\ud83d\udc49"},raised_hands:{code:":raised_hands:",emoji:"\ud83d\ude4c"},pray:{code:":pray:",emoji:"\ud83d\ude4f"},point_up_2:{code:":point_up_2:",emoji:"\ud83d\udc46"},clap:{code:":clap:",emoji:"\ud83d\udc4f"},muscle:{code:":muscle:",emoji:"\ud83d\udcaa"},metal:{code:":metal:",emoji:"\ud83e\udd18"},fu:{code:":fu:",emoji:"\ud83d\udd95"},walking:{code:":walking:",emoji:"\ud83d\udeb6"},runner:{code:":runner:",emoji:"\ud83c\udfc3"},running:{code:":running:",emoji:"\ud83c\udfc3"},couple:{code:":couple:",emoji:"\ud83d\udc6b"},family:{code:":family:",emoji:"\ud83d\udc6a"},two_men_holding_hands:{code:":two_men_holding_hands:",emoji:"\ud83d\udc6c"},two_women_holding_hands:{code:":two_women_holding_hands:",emoji:"\ud83d\udc6d"},dancer:{code:":dancer:",emoji:"\ud83d\udc83"},dancers:{code:":dancers:",emoji:"\ud83d\udc6f"},ok_woman:{code:":ok_woman:",emoji:"\ud83d\ude46"},no_good:{code:":no_good:",emoji:"\ud83d\ude45"},information_desk_person:{code:":information_desk_person:",emoji:"\ud83d\udc81"},raising_hand:{code:":raising_hand:",emoji:"\ud83d\ude4b"},bride_with_veil:{code:":bride_with_veil:",emoji:"\ud83d\udc70"},person_with_pouting_face:{code:":person_with_pouting_face:",emoji:"\ud83d\ude4e"},person_frowning:{code:":person_frowning:",emoji:"\ud83d\ude4d"},bow:{code:":bow:",emoji:"\ud83d\ude47"},couplekiss:{code:":couplekiss:",emoji:"\ud83d\udc8f"},couple_with_heart:{code:":couple_with_heart:",emoji:"\ud83d\udc91"},massage:{code:":massage:",emoji:"\ud83d\udc86"},haircut:{code:":haircut:",emoji:"\ud83d\udc87"},nail_care:{code:":nail_care:",emoji:"\ud83d\udc85"},boy:{code:":boy:",emoji:"\ud83d\udc66"},girl:{code:":girl:",emoji:"\ud83d\udc67"},woman:{code:":woman:",emoji:"\ud83d\udc69"},man:{code:":man:",emoji:"\ud83d\udc68"},baby:{code:":baby:",emoji:"\ud83d\udc76"},older_woman:{code:":older_woman:",emoji:"\ud83d\udc75"},older_man:{code:":older_man:",emoji:"\ud83d\udc74"},person_with_blond_hair:{code:":person_with_blond_hair:",emoji:"\ud83d\udc71"},man_with_gua_pi_mao:{code:":man_with_gua_pi_mao:",emoji:"\ud83d\udc72"},man_with_turban:{code:":man_with_turban:",emoji:"\ud83d\udc73"},construction_worker:{code:":construction_worker:",emoji:"\ud83d\udc77"},cop:{code:":cop:",emoji:"\ud83d\udc6e"},angel:{code:":angel:",emoji:"\ud83d\udc7c"},princess:{code:":princess:",emoji:"\ud83d\udc78"},smiley_cat:{code:":smiley_cat:",emoji:"\ud83d\ude3a"},smile_cat:{code:":smile_cat:",emoji:"\ud83d\ude38"},heart_eyes_cat:{code:":heart_eyes_cat:",emoji:"\ud83d\ude3b"},kissing_cat:{code:":kissing_cat:",emoji:"\ud83d\ude3d"},smirk_cat:{code:":smirk_cat:",emoji:"\ud83d\ude3c"},scream_cat:{code:":scream_cat:",emoji:"\ud83d\ude40"},crying_cat_face:{code:":crying_cat_face:",emoji:"\ud83d\ude3f"},joy_cat:{code:":joy_cat:",emoji:"\ud83d\ude39"},pouting_cat:{code:":pouting_cat:",emoji:"\ud83d\ude3e"},japanese_ogre:{code:":japanese_ogre:",emoji:"\ud83d\udc79"},japanese_goblin:{code:":japanese_goblin:",emoji:"\ud83d\udc7a"},see_no_evil:{code:":see_no_evil:",emoji:"\ud83d\ude48"},hear_no_evil:{code:":hear_no_evil:",emoji:"\ud83d\ude49"},speak_no_evil:{code:":speak_no_evil:",emoji:"\ud83d\ude4a"},guardsman:{code:":guardsman:",emoji:"\ud83d\udc82"},skull:{code:":skull:",emoji:"\ud83d\udc80"},feet:{code:":feet:",emoji:"\ud83d\udc3e"},lips:{code:":lips:",emoji:"\ud83d\udc44"},kiss:{code:":kiss:",emoji:"\ud83d\udc8b"},droplet:{code:":droplet:",emoji:"\ud83d\udca7"},ear:{code:":ear:",emoji:"\ud83d\udc42"},eyes:{code:":eyes:",emoji:"\ud83d\udc40"},nose:{code:":nose:",emoji:"\ud83d\udc43"},tongue:{code:":tongue:",emoji:"\ud83d\udc45"},love_letter:{code:":love_letter:",emoji:"\ud83d\udc8c"},bust_in_silhouette:{code:":bust_in_silhouette:",emoji:"\ud83d\udc64"},busts_in_silhouette:{code:":busts_in_silhouette:",emoji:"\ud83d\udc65"},speech_balloon:{code:":speech_balloon:",emoji:"\ud83d\udcac"},thought_balloon:{code:":thought_balloon:",emoji:"\ud83d\udcad"},sunny:{code:":sunny:",emoji:"\u2600\ufe0f"},umbrella:{code:":umbrella:",emoji:"\u2614\ufe0f"},cloud:{code:":cloud:",emoji:"\u2601\ufe0f"},snowflake:{code:":snowflake:",emoji:"\u2744\ufe0f"},snowman:{code:":snowman:",emoji:"\u26c4\ufe0f"},zap:{code:":zap:",emoji:"\u26a1\ufe0f"},cyclone:{code:":cyclone:",emoji:"\ud83c\udf00"},foggy:{code:":foggy:",emoji:"\ud83c\udf01"},ocean:{code:":ocean:",emoji:"\ud83c\udf0a"},cat:{code:":cat:",emoji:"\ud83d\udc31"},dog:{code:":dog:",emoji:"\ud83d\udc36"},mouse:{code:":mouse:",emoji:"\ud83d\udc2d"},hamster:{code:":hamster:",emoji:"\ud83d\udc39"},rabbit:{code:":rabbit:",emoji:"\ud83d\udc30"},wolf:{code:":wolf:",emoji:"\ud83d\udc3a"},frog:{code:":frog:",emoji:"\ud83d\udc38"},tiger:{code:":tiger:",emoji:"\ud83d\udc2f"},koala:{code:":koala:",emoji:"\ud83d\udc28"},bear:{code:":bear:",emoji:"\ud83d\udc3b"},pig:{code:":pig:",emoji:"\ud83d\udc37"},pig_nose:{code:":pig_nose:",emoji:"\ud83d\udc3d"},cow:{code:":cow:",emoji:"\ud83d\udc2e"},boar:{code:":boar:",emoji:"\ud83d\udc17"},monkey_face:{code:":monkey_face:",emoji:"\ud83d\udc35"},monkey:{code:":monkey:",emoji:"\ud83d\udc12"},horse:{code:":horse:",emoji:"\ud83d\udc34"},racehorse:{code:":racehorse:",emoji:"\ud83d\udc0e"},camel:{code:":camel:",emoji:"\ud83d\udc2b"},sheep:{code:":sheep:",emoji:"\ud83d\udc11"},elephant:{code:":elephant:",emoji:"\ud83d\udc18"},panda_face:{code:":panda_face:",emoji:"\ud83d\udc3c"},snake:{code:":snake:",emoji:"\ud83d\udc0d"},bird:{code:":bird:",emoji:"\ud83d\udc26"},baby_chick:{code:":baby_chick:",emoji:"\ud83d\udc24"},hatched_chick:{code:":hatched_chick:",emoji:"\ud83d\udc25"},hatching_chick:{code:":hatching_chick:",emoji:"\ud83d\udc23"},chicken:{code:":chicken:",emoji:"\ud83d\udc14"},penguin:{code:":penguin:",emoji:"\ud83d\udc27"},turtle:{code:":turtle:",emoji:"\ud83d\udc22"},bug:{code:":bug:",emoji:"\ud83d\udc1b"},honeybee:{code:":honeybee:",emoji:"\ud83d\udc1d"},ant:{code:":ant:",emoji:"\ud83d\udc1c"},beetle:{code:":beetle:",emoji:"\ud83d\udc1e"},snail:{code:":snail:",emoji:"\ud83d\udc0c"},octopus:{code:":octopus:",emoji:"\ud83d\udc19"},tropical_fish:{code:":tropical_fish:",emoji:"\ud83d\udc20"},fish:{code:":fish:",emoji:"\ud83d\udc1f"},whale:{code:":whale:",emoji:"\ud83d\udc33"},whale2:{code:":whale2:",emoji:"\ud83d\udc0b"},dolphin:{code:":dolphin:",emoji:"\ud83d\udc2c"},cow2:{code:":cow2:",emoji:"\ud83d\udc04"},ram:{code:":ram:",emoji:"\ud83d\udc0f"},rat:{code:":rat:",emoji:"\ud83d\udc00"},water_buffalo:{code:":water_buffalo:",emoji:"\ud83d\udc03"},tiger2:{code:":tiger2:",emoji:"\ud83d\udc05"},rabbit2:{code:":rabbit2:",emoji:"\ud83d\udc07"},dragon:{code:":dragon:",emoji:"\ud83d\udc09"},goat:{code:":goat:",emoji:"\ud83d\udc10"},rooster:{code:":rooster:",emoji:"\ud83d\udc13"},dog2:{code:":dog2:",emoji:"\ud83d\udc15"},pig2:{code:":pig2:",emoji:"\ud83d\udc16"},mouse2:{code:":mouse2:",emoji:"\ud83d\udc01"},ox:{code:":ox:",emoji:"\ud83d\udc02"},dragon_face:{code:":dragon_face:",emoji:"\ud83d\udc32"},blowfish:{code:":blowfish:",emoji:"\ud83d\udc21"},crocodile:{code:":crocodile:",emoji:"\ud83d\udc0a"},dromedary_camel:{code:":dromedary_camel:",emoji:"\ud83d\udc2a"},leopard:{code:":leopard:",emoji:"\ud83d\udc06"},cat2:{code:":cat2:",emoji:"\ud83d\udc08"},poodle:{code:":poodle:",emoji:"\ud83d\udc29"},paw_prints:{code:":paw_prints:",emoji:"\ud83d\udc3e"},bouquet:{code:":bouquet:",emoji:"\ud83d\udc90"},cherry_blossom:{code:":cherry_blossom:",emoji:"\ud83c\udf38"},tulip:{code:":tulip:",emoji:"\ud83c\udf37"},four_leaf_clover:{code:":four_leaf_clover:",emoji:"\ud83c\udf40"},rose:{code:":rose:",emoji:"\ud83c\udf39"},sunflower:{code:":sunflower:",emoji:"\ud83c\udf3b"},hibiscus:{code:":hibiscus:",emoji:"\ud83c\udf3a"},maple_leaf:{code:":maple_leaf:",emoji:"\ud83c\udf41"},leaves:{code:":leaves:",emoji:"\ud83c\udf43"},fallen_leaf:{code:":fallen_leaf:",emoji:"\ud83c\udf42"},herb:{code:":herb:",emoji:"\ud83c\udf3f"},mushroom:{code:":mushroom:",emoji:"\ud83c\udf44"},cactus:{code:":cactus:",emoji:"\ud83c\udf35"},palm_tree:{code:":palm_tree:",emoji:"\ud83c\udf34"},evergreen_tree:{code:":evergreen_tree:",emoji:"\ud83c\udf32"},deciduous_tree:{code:":deciduous_tree:",emoji:"\ud83c\udf33"},chestnut:{code:":chestnut:",emoji:"\ud83c\udf30"},seedling:{code:":seedling:",emoji:"\ud83c\udf31"},blossom:{code:":blossom:",emoji:"\ud83c\udf3c"},ear_of_rice:{code:":ear_of_rice:",emoji:"\ud83c\udf3e"},shell:{code:":shell:",emoji:"\ud83d\udc1a"},globe_with_meridians:{code:":globe_with_meridians:",emoji:"\ud83c\udf10"},sun_with_face:{code:":sun_with_face:",emoji:"\ud83c\udf1e"},full_moon_with_face:{code:":full_moon_with_face:",emoji:"\ud83c\udf1d"},new_moon_with_face:{code:":new_moon_with_face:",emoji:"\ud83c\udf1a"},new_moon:{code:":new_moon:",emoji:"\ud83c\udf11"},waxing_crescent_moon:{code:":waxing_crescent_moon:",emoji:"\ud83c\udf12"},first_quarter_moon:{code:":first_quarter_moon:",emoji:"\ud83c\udf13"},waxing_gibbous_moon:{code:":waxing_gibbous_moon:",emoji:"\ud83c\udf14"},full_moon:{code:":full_moon:",emoji:"\ud83c\udf15"},waning_gibbous_moon:{code:":waning_gibbous_moon:",emoji:"\ud83c\udf16"},last_quarter_moon:{code:":last_quarter_moon:",emoji:"\ud83c\udf17"},waning_crescent_moon:{code:":waning_crescent_moon:",emoji:"\ud83c\udf18"},last_quarter_moon_with_face:{code:":last_quarter_moon_with_face:",emoji:"\ud83c\udf1c"},first_quarter_moon_with_face:{code:":first_quarter_moon_with_face:",emoji:"\ud83c\udf1b"},moon:{code:":moon:",emoji:"\ud83c\udf14"},earth_africa:{code:":earth_africa:",emoji:"\ud83c\udf0d"},earth_americas:{code:":earth_americas:",emoji:"\ud83c\udf0e"},earth_asia:{code:":earth_asia:",emoji:"\ud83c\udf0f"},volcano:{code:":volcano:",emoji:"\ud83c\udf0b"},milky_way:{code:":milky_way:",emoji:"\ud83c\udf0c"},partly_sunny:{code:":partly_sunny:",emoji:"\u26c5\ufe0f"},bowtie:{code:":bowtie:",emoji:"\ud83d\udc54"}},ezmoji.check=function(a){for(var b in ezmoji.list)if(a.innerText.includes(ezmoji.list[b].code)){var c=a.innerHTML.replace(ezmoji.list[b].code,ezmoji.list[b].emoji);return a.innerHTML=c}},ezmoji.init=function(a){for(var b=a.childNodes,c=0;c<b.length;c++)b[c]&&b[c].childNodes.length>0&&(ezmoji.init(b[c]),ezmoji.check(b[c]))},window.addEventListener("load",ezmoji.init(document));
</script>
```

### License
MIT License

Copyright (c) 2019 Michael Arakilian

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.