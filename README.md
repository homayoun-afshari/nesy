# Neuro-Symbolic Artificial Intelligence for Visual Reasoning via Dynamic Logic Tensor Networks

## A Bit of History

<p align="justify">
 If you're new to Artificial Intelligence (AI), you might think Neural Networks (NNs) are the whole <i>enchilada</i>. You might even believe AI and NNs are practically the same thing. Well, you're almost right! In a way, that's a fair assumption if we're talking <i>modern AI</i>, which is basically a love letter to neural methods. Most of the field is obsessed with training and tweaking those glorious neurons. But hold on; the history of AI tells a bit different story. Once upon a time, AI was all about <i>logical rules</i>, fondly known as <a href="https://en.wikipedia.org/wiki/GOFAI">Good-Old-Fashioned AI (GOFAI)</a>. And, my goodness, those methods worked like a charm! For instance, they powered expert systems that could reason through problems with the precision of a mathematician solving a crossword puzzle.
</p>

<p align="center">
 <img src="readme_files/gofai.webp" width="500px">
 <br>
 <i>From "<a href="https://billwadge.com/2024/02/12/the-rise-and-fall-of-gofai/">The Rise and Fall of GOFAI</a>" by Bill Wadge</i>
</p>

<p align="justify">
 However, these days, GOFAI is like that retro band you loved in the '90s; rarely heard but fondly remembered. So, what happened? Did we ditch it? You bet we did! Like all good things, GOFAI birthed modern AI and then slipped into the shadows. Why? Well, neural networks swooped in with their data-crunching superpowers, learning everything from cat pics to quantum physics <i>without needing hand-crafted rules</i>. They were flashy, flexible, and frankly, too cool to resist. Also, GOFAI's rigid logic <i>couldn't keep up</i> with the big data party, so it took a backseat. But now, as we teeter on the edge of Artificial General Intelligence (AGI), we're dusting off GOFAI's playbook. Those logical roots are making a comeback, because, let's face it, learning is great, but reasoning like a human is <i>the real jackpot</i>. After all, as the old saying goes, "the creaking gate hangs longest". So, buckle up for a new brand of AI!
</p>

## NeSy AI

<p align="justify">
 How did we revive GOFAI? Enter Neuro-Symbolic (NeSy) AI, the <i>lovechild</i> of NNs and symbolic reasoning, ready to party like it’s 2099. You already know NNs, so let's talk about the other half. Symbolic reasoning is the art of <i>thinking with symbols</i>, like a brainy game of chess where each piece stands for something meaningful, like "cat", "danger", or "pizza". A symbol, in this context, is a tidy little <i>package of meaning</i>, which could be a word, number, or concept that represents something in the real world. For example, picture a robot spotting a furry creature and reasoning: “Furry + meows = probably a cat, not a toaster.” That's symbolic reasoning at work, using clear-cut rules to make sense of the world.
</p>

<p align="justify">
 NeSy AI <i>marries</i> this logical wizardry with a NN's knack for spotting patterns in messy data, like recognizing a cat in a blurry photo, which means giving your NN a PhD in logic while keeping its data-crunching vibes. Cool, right? It becomes even cooler to know this combo works for a good reason. Cognitive science tells us our brains use <i>two systems</i> for thinking. System 1, the <i>Homer Simpson of AI</i>, is your gut instinc; quick, intuitive, and great at spotting patterns in data to apply to new situations. System 2, the <i>Sherlock Holmes of AI</i>, is your beautiful problem-solving mind; deep, deliberate, and powerful at reasoning through data like a sharp knife trhough butter. NeSy does both: its neural part learns from data (System 1) and its symbolic part reasons about it (System 2). But, how do we actually do NeSy AI? We'll dive into that rabbit hole next.
</p>

## NeSy Frameworks

<p align="justify">
 Over the past few years, a parade of NeSy methods has marched onto the scene. Since NeSy is more a paradigm than a single trick up the AI sleeve, these methods double as frameworks, each with its own quirky way of blending neural networks with symbolic reasoning. Want the full scoop? Check out <a href="https://harshakokel.com/posts/neurosymbolic-systems/">Types of Neuro-Symbolic Systems</a>, which lays out Kautz’s six-level taxonomy of NeSy like a map for AI treasure hunters. The big takeaway? These frameworks aren’t just slapping neural and symbolic together like a PB&J sandwich—they’re carefully engineering systems to reason and learn in harmony, often grounding abstract logic in real-world data. For a deeper dive, sneak a peek at  <a href="https://arxiv.org/abs/2305.00813">Neurosymbolic AI - Why, What, and How</a>.
</p>

<p align="justify">
 Among these frameworks, my personal rockstar is <a href="https://arxiv.org/abs/2012.13635">Logic Tensor Networks</a>, which is actually the one I worked on during my thesis. To get LTNs, we first need to know with First-Order Logic (FOL). Think of FOL as the language of logic, letting us craft statements like, "If it's furry and meows, it's a cat" or "is_furry(x) & is_meowing(x) → is_cat(x)". The latter is an FOL statement, a tidy rule for reasoning. LTNs take these FOL statements and magically transform them into NNs. Train that network, and boom! The logical rule gets applied to any data you throw at it, like a brainy autopilot for reasoning.
</p>

<p align="justify">
 The kicker? Training a NeSy system isn’t your typical neural network rodeo. Take, for example, the task I tackled in my thesis: <a href="https://par.nsf.gov/servlets/purl/10440135">Visual Sudoku Puzzle Classification</a>. Picture a pile of labeled correct and incorrect Sudoku boards, where the model learns to classify them, but with a big twist: the supervision is on the labels, not the digits themselves. Oh, and the digits might not even be numbers. They can be English letters, Japanese signs, or even fashion items. Tricky, right? I'll spill more details on this puzzle later. The point is, NeSy systems shine when trained end-to-end, weaving together learning and reasoning like a cosmic tapestry.
</p>

## Challenge

## Conceptual Solution

## Practical Solution

## Running the Codes

### Initialization

### Data Preparation

### Main Algorithm

## Acknoledgement

