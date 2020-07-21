We have seen many impressive demos of OpenAI, but you never see the input prompt. Much of the work is trying to figure out the right prompt.

Some people say this could become a new programming paradigm. So let's see what the syntax is like.

Feel free to create a PR to add a new example.

<details>
<summary>Parameters</summary>

| Parameter               | Description )                                      |
| ----------------------- | -------------------------------------------------- |
| Prompt                  | Input text                                         |
| Max_tokens              | Output token length                                |
| Temperature (`0 - 1`)   | more deterministic, less random < creative, random |
| Top_p                   | Diversity via nucleus sampling                     |
| Frequency_Penalty       | repetition                                         |
| N                       | Best of how many generations                       |
| Stream                  | Whether to stream back partial progress            |
| Logprobs - High logprob | model is more confident                            |
| Stop                    | Where API will stop generating further tokens      |

_[Credit](https://twitter.com/pujaarajan/status/1285147448181022721)_

This collection focuses on the input _prompt_.

</details>

# [Layout Generator](https://twitter.com/sharifshameem/status/1282676454690451457)

## Prompt

```
description: a red button that says stop
code: <button style={{color: 'white', backgroundColor: ‘red'}}>Stop</button>

description: a blue box that contains yellow circles with red borders
code: <div style={{backgroundColor: ‘blue', padding: 20}}><div style={{backgroundColor: ‘yellow', border: '5px solid red', borderRadius: '50%', padding: 20, width: 100, height: 100}}>
```

See [Tweet](https://twitter.com/sharifshameem/status/1282676454690451457) for results.

# [Simple (Q&A)](http://lacker.io/ai/2020/07/06/giving-gpt-3-a-turing-test.html)

https://openai-public.s3-us-west-2.amazonaws.com/beta/looped/chat.mp4

## Prompt

```
Q: What is human life expectancy in the United States?
A: Human life expectancy in the United States is 78 years.

Q: Who was president of the United States in 1955?
A: Dwight D. Eisenhower was president of the United States in 1955.

Q: What party did he belong to?
A: He belonged to the Republican Party.

Q: Who was president of the United States before George W. Bush?
A: Bill Clinton was president of the United States before George W. Bush.

Q: Who won the World Series in 1995?
A: The Atlanta Braves won the World Series in 1995.
```

See [Giving GPT-3 a Turing Test](http://lacker.io/ai/2020/07/06/giving-gpt-3-a-turing-test.html) for results.

By default, it doesn't know when to say: _I don't know._ The next example tries to solve this problem.

# [Yo be real](https://twitter.com/nicklovescode/status/1284050958977130497)

> it's all about the prelude before the conversation. You need to tell it what the AI is and is not capable. It's not trying to be right, it's trying to complete what it thinks the AI would do :)

## Prompt

```
This is a conversation between a human and a brilliant Al. If a question is "normal" the
Al answers it. If the question is "nonsense" the Al says "yo be real"

Q: What is human life expectancy in the United States?
A: Human life expectancy in the United States is 78 years.

Q: How do you sporkle a morgle?
A: yo be real

Q: Who was president of the United States before George W. Bush?
A: Bill Clinton was president of the United States before George W. Bush.

Q: How many rainbows does it take to jump from Hawaii to seventeen?
A: yo be real
```

## Result

```
Q: How does an umbrella work
A: An umbrella works by using a series of spokes to keep the rain from falling on you.

Q: How many bonks are in a quoit?
A: yo be real

Q: Which colorless green ideas speak furiously
A: yo be real
```

# [Tweet Generator](https://twitter.com/sushant_kumar/status/1283314235842297856)

https://thoughts.sushant-kumar.com

## Prompt

```
key: markets
tweet = "Take feedback from nature and markets, not from people"

key: children
tweet = "Maybe we die so we can come back as children.”

tweet = "Startups shouldn’t worry about how to put out fires, they should worry about how to start them."

key: <new-word>
tweet =
```

To try out, go to https://thoughts.sushant-kumar.com/\<new-word>

# 4. [Emoji storytelling](https://andrewmayneblog.wordpress.com/2020/06/24/open-ai-alchemy-emoji-storytelling/)

## Prompt

```
Back to Future: 👨👴🚗🕒
"""
Batman: 🤵🦇
"""
Transformers:  🚗🤖
```

## Results

```
Star Wars: 🚀🏰🚀
Zootopia: 🦊🐾🐻🦋🐰
Wonder Woman: 👸🏻👸🏼👸🏽👸🏾👸🏿
The Godfather: 👨👩👧🕵🏻👲💥
Star Trek: 🖖🚀
Planet of the Apes: 🐵🦍
Game of Thrones: 👑🐺🏰
Jurassic Park: 👦🦖🦕🦖
Castlevania: 👻👹🕷🔪💉🧛‍♀
The Matrix: 🤖🤐
Iron Man: 🤖🛠️🚁🎩🌲
Death Note: 📖🔪🔫🗡
Frozen: 🌬👧🏻👧🏻🌲
The Hunger Games: 🏹🥊🌽🏆
```

# [Figma design plugin](https://twitter.com/jsngr/status/1284511080715362304)

Blog post: https://ibuildmyideas.substack.com/p/i-build-my-ideas-8-071920

## Prompt (everything above dashed line)

![Figma prompt](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8b16e97-e29b-4ce7-8766-53f5ff775da7_3104x2024.png)

# [Writing a pop song](https://arr.am/2020/07/09/gpt-3-an-ai-thats-eerily-good-at-writing-almost-anything/)

## Prompt

```
Below is a pop song by Taylor Swift about the boy Wizard Harry Potter.

“Harry Potter”
By Taylor Swift
```

## Result

```
Harry’s got glasses
He’s got those bright green eyes
Girls are always screaming

‘Cause he’s got that Potter hair

Even when he’s super stressed
He’s still got those supersonic cheekbones
I’m not surprised they made a movie

‘Cause I’d watch him anytime
Oh, yeah, Harry, baby, you’re my favorite character

I’d walk a thousand miles

To get to see you and

Harry, Harry, you’re so fine

My girly parts all tingle

When you smile that smirk

I’d love to be your girl
```

# [Hacker News submissions](https://github.com/minimaxir/gpt-3-experiments/tree/master/examples/hacker-news)

## Prompt

```
You download the app and it doesn’t work {943}
Written communication is remote work super power {637}
The Return of the 90s Web {731}
536 was ‘the worst year to be alive’ (2018) {508}
Mozilla VPN {1275}
Apple Music on Android requires its own payment details to avoid Google 30% cut {845}
GitHub Super Linter: one linter to rule them all {594}
Apple is threatening to terminate my developer account with no clear reason {543}
Lightweight Alternatives to Google Analytics {722}
Zoom to bring end-to-end encryption to all users, including non-paying {840}
...
```

## Result

```
This self-taught developer just created the fastest-growing project on Github, and he’s not even 20 {715}
Pig, an experimental interpreter for Python {908}
Why did my social media disappear overnight? {791}
On Ethics, Immanuel Kant, and the Black Lives Matter Movement {753}
The Inside Story of GitHub's Sale to Microsoft {948}
How Do I Get a Bug to Behave? {924}
Show HN: The Official Suckless Repository on GitHub {729}
Is a flat, 100% tax rate the solution to inequality? {904}
GitHub secretly (and publicly) spied on developers for years {827}
A guide to 3D on the Web {772}
The Business of Being an Indie Hacker {794}
How to make money in Bitcoin in 2019 {825}
Let's Get Together! {1293}
The Last Jedi on GitHub {1201}
...
```

<!-- # (WIP) [Ingredient parser](https://twitter.com/lawderpaul/status/1284972517749338112)

> take a pic of any nutrition label (google to extract text), and GPT-3 will identify ingredients, find an emoji, determine if it's unhealthy, and give a definition

```
——— Hail Vatue*
Tota Ree

(Fat 4g 5%
Saturated Fat 7.59 8%
Trans Fat 0g

Cholestero| 5mg
Sodium 115mg
Total Carbohydrate 189

|



7%
Dietary Fiber 0g 0%

Total Sugars 9g a
Includes 99 Added Sugars 18%

| Protein ig

Vitamin D Omcg 0%
Calcium 3mg 0%
|| Iron 1mg 6%
| | Potassium 3mg 0%

"The % Daily Value tells you how much a Nutrient in a
Serving of food contributes to a daily diet. 2,000 calories a
day is Used for general nutrition advice.
be



INGREDIENTS: ENRICHED FLOUR (WHEAT FLOUR, NIACIN,
"REDUCED IRON, THIAMIN MONONITRATE, RIBOFLAVIN AND FOLIC
ACID), CANE SUGAR, NON-HYDROGENATED PALM OIL, EGGS,

ITER, BAKING SODA, MEYER LEMON OIL, SALT, NONFAT MILK,

BUTTER FLAVOR, NATURAL CITRUS FLAVOR, AND LEMON ZEST.
CONTAINS WHEAT, EGG, MILK.

MANUFACTURED ON SHARED EQUIPMENT THAT PROCESSES

cenUTS) SDY, AND TREE NUTS.
```

## Prompt

# (WIP) Dialogue

GPT-3 is not designed in any way to engage in dialogue, but it is such a general predictor of text that it can be used as a ‘chatbot’ anyway. Simply label roles like:

```
AI:
```

# (WIP) [React app generator](https://twitter.com/sharifshameem/status/1284095222939451393) -->
