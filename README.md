# Neuro-Symbolic Artificial Intelligence for Visual Reasoning via Dynamic Logic Tensor Networks

## A Bit of History

<p align="justify">
 If you're new to Artificial Intelligence (AI), you might think Neural Networks (NNs) are the <i>whole</i> story. You might even believe AI and NNs are practically the same thing. Well, you're almost right! In a way, that's a fair assumption if we're talking <i>modern AI</i>, which is basically a love letter to neural methods. In fact, most of the field is obsessed with training and tweaking those glorious neurons. However, the history of AI tells a different story. Once upon a time, AI was <i>all</i> about logical rules, fondly known as <a href="https://en.wikipedia.org/wiki/GOFAI">Good-Old-Fashioned AI (GOFAI)</a>. And, my goodness, those methods worked like a <i>charm</i>! For instance, <a href="https://en.wikipedia.org/wiki/El_Ajedrecista">El Ajedrecista</a>, the Quevedo's chess automaton could play king-and-rook endgames entirely on its own in 1912.
</p>

<p align="center">
 <img src="readme_files/gofai.webp" width="500px">
 <br>
 <i>From "<a href="https://billwadge.com/2024/02/12/the-rise-and-fall-of-gofai/">The Rise and Fall of GOFAI</a>" by Bill Wadge</i>
</p>

<p align="justify">
 However, these days, GOFAI is like that retro band in the '90s; rarely heard but fondly remembered. So, what happened? Well, modern AI was born! Like all good things, GOFAI slipped into the shadows, and then, NNs swooped in with their data-crunching superpowers, learning everything from cat pics to quantum physics <i>without</i> needing hand-crafted rules. They were flashy, flexible, and frankly, too cool to resist. Also, GOFAI's rigid logic <i>couldn't</i> keep up with the big data party, so it took a backseat. But now, as we teeter on the edge of Artificial General Intelligence (AGI), we're dusting off GOFAI's playbook. Those logical roots are making a comeback, because, let's face it, learning is great, but GOFAI's human-like reasoning is the real <i>jackpot</i>. After all, as the old saying goes, <q>the creaking gate hangs longest</q>. So, buckle up for a new brand of AI!
</p>

## NeSy AI

<p align="justify">
 How did we revive GOFAI? Enter Neuro-Symbolic (NeSy) AI, the <i>lovechild</i> of NNs and symbolic reasoning. You already know NNs, so let's talk about the other half. Picture a robot spotting a furry creature and reasoning: <i>Furry + meows = probably a cat, not a toaster</i>. That's symbolic reasoning at work, using clear-cut rules to make sense of the world. In fact, symbolic reasoning is the <i>art</i> of thinking with symbols. A symbol, in this context, is a tidy little <i>package</i> of meaning, which could be a word, number, or concept that represents something in the real world. For example, in a brainy game of chess, each piece stands for something meaningful, like a <i>pawn</i>, <i>knight</i>, or <i>queen</i>.
</p>

<p align="justify">
 NeSy AI <i>marries</i> this logical wizardry with a NN's knack for spotting patterns in messy data, which means giving your NN a PhD in logic while keeping its data-crunching vibes. Cool, right? It becomes even cooler to know this combo works for a good reason. Cognitive science tells us our brains use <i>two</i> systems for thinking. System 1 is your gut instinc; quick, intuitive, and great at spotting patterns in data to apply to new situations. System 2, the <i>Sherlock Holmes of AI</i>, is your beautiful problem-solving mind; deep, deliberate, and powerful at reasoning. NeSy does both: its neural part learns from data (System 1) and its symbolic part reasons about it (System 2).
</p>

<p align="justify">
  But, how do we actually do NeSy AI? Training a NeSy system isn't your typical NN <i>rodeo</i>. Take, for example, the task I tackled in my thesis: <a href="https://par.nsf.gov/servlets/purl/10440135">Visual Sudoku Puzzle Classification</a>, where the model learns to classify a pile of labeled correct and incorrect Sudoku boards but with a big twist: the supervision is only on the <i>labels</i> not the digits themselves. Oh, and the digits might not even be numbers. They can be English letters, Japanese signs, or even fashion items. Tricky, right? I'll spill more details on this puzzle later. The point is, NeSy frameworks shine when trained end-to-end, weaving together learning and reasoning like a cosmic tapestry.
</p>

## NeSy Frameworks

<p align="justify">
 Over the past few years, a <i>parade</i> of NeSy methods has marched onto the scene. Since NeSy is more a <i>paradigm</i> than a single trick up the AI sleeve, these methods double as frameworks, each with its own quirky way of blending NNs with symbolic reasoning. Check out <a href="https://harshakokel.com/posts/neurosymbolic-systems/">Types of Neuro-Symbolic Systems</a>, which lays out <i>Kautz's six-level taxonomy of NeSy</i>. The big takeaway? These frameworks aren't just slapping neural and symbolic together like a sandwich; they're <i>carefully</i> engineering systems to reason and learn in harmony. For a deeper dive, also sneak a peek at <a href="https://arxiv.org/abs/2305.00813">Neurosymbolic AI - Why, What, and How</a>.
</p>

<p align="justify">
 Among those frameworks, my personal favorite is <a href="https://arxiv.org/abs/2012.13635">Logic Tensor Networks</a>, which is actually the one I also worked on during my thesis. To get LTNs, we first need to know First-Order Logic (FOL). Think of it as the <i>language</i> of logic, which lets us craft statements like <i>If it's furry and meows, it's a cat</i> or <i>is_furry(x) & is_meowing(x) → is_cat(x)</i>. The latter is literally an FOL statement: a tidy rule for symbolic reasoning. LTNs take these FOL statements and gracefully transform them into NNs. Train that network, and boom! The logical rule gets applied to any data you throw at it.
</p>

<p align="justify">
 Now, you might wonder how these rigid binary FOL statements fit into the squishy floating-point world of NNs. That's where it gets interesting. You know <a href="https://en.wikipedia.org/wiki/Fuzzy_logic">Fuzzy Logic</a>, right? That's how! The brilliance of LTNs comes from <i>grounding</i>: a process that relaxes those hard all-or-nothing statements into something softer and more flexible. For example, take again the statement <i>is_furry(x) & is_meowing(x) → is_cat(x)</i>. LTNs use fuzzy logic to encode this into a NN, allowing it to handle uncertainty and partial truths, like a wise sage navigating life's gray areas and deciding that being almost furry and meowing time-to-time implies being almost a cat, and much less confidently, a broken toaster, which happens to be furry for unknown reasons!
</p>

## Challenge

<p align="justify">
 NeSy systems are the <i>bee's knees</i>, and <a href="https://www.linkedin.com/posts/gary-marcus-b6384b4_how-o3-and-grok-4-accidentally-vindicated-activity-7350215211166953472-iN8p">some</a> even believe the <i>next</i> paradigm shift in AI will come courtesy of NeSy. However, another old saying goes, <q>every coin has two sides</q>. There are still hurdles to jump, and for my thesis, I focused on a <i>triple-threat challenge</i> in current NeSy visual reasoning frameworks. But before jumping into that rabbit hole, let's quickly review visual reasoning.
</p>

<p align="justify">
 Visual reasoning is AI's version of playing visual detective; taking in images and <i>not just</i> seeing them, but <i>also</i> understanding what they mean logically. It's like asking your AI to scan a scene an image of a cat to deduce whether it's plotting world domination or just napping. And, that's actually the reason why I chose to study the Sudoku task during my thesis: the task is about both <i>seeing</i> the board and <i>detecting</i> if it follows the no-repeats-in-row-or-column rule.
</p>

<p align="justify">
 Okay, let's now unpack that triple-threat challenge. The first prong: some approaches are slick <i>but</i> stubborn, locked into a fixed set of logical rules with zero wiggle room to adapt to new ones. The second: others are more flexible, dynamically extracting underlying logical rules from data; <i>but</i> good luck explaining what they even are! The third: newer systems have tried to bridge this gap, <i>but</i> their rules lack formality; meaning they're too wordy for machines to verify without a human poking around. So, the million-dollar question is: can we build a NeSy system for visual reasoning that's flexible, explainable, and formal, <i>all at once</i>?
</p>

## Conceptual Solution

<p align="justify">
 My <i>general</i> idea to crack this challenge is the system sketched below. It kicks off with two inputs: textual data (optional instructions or descriptions) and visual data (the actual images). These get tossed into a context generator, which mashes them together into a unified context. From there, a rule generator grabs this context and whips up symbolic rules. Meanwhile, the visual input is also fed into a visual processor to cook up visual symbols. Then, a rule verifier swoops in, applying those symbolic rules to the visual symbols to deliver the final output.
</p>

<p align="center">
 <img src="readme_files/conceptual.png" width="500px">
</p>

<p align="justify">
 Now, here's where the party starts: the final output loops back into the context generator, acting like a mid-game coach dishing out <i>feedback</i>. This means the system can spot its own fumbles and <i>fix</i> them on the fly; sort of inspired by Reinforcement Learning (RL). Plus, the rule generator itself gets in on the feedback action, tweaking its own rules if things go off the rails. This setup targets the trifecta I mentioned earlier: it's flexible (adapts to different tasks), explainable (rules are in clear symbolic language, not mathematical tensor nightmares), and formal (rules are machine-verifiable, no human babysitting required).
</p>

## Functional Solution

<p align="justify">
 Alright, let's get down to the nuts and bolts of how this idea comes to life. Depending on the functional designs <i>you pick</i> for each module described, there are many ways to pull this off. For my thesis, given the time and resources I had, I went for the simplest setup I could find. As shown in the figure below, I used a prompt engineer to carve prompts and act as the context generator. Then, a Vision Language Model (VLM) took those prompts and churned out symbolic rules in FOL. For the visual processor, I leaned on a straightforward Convolutional Neural Network (CNN) and used its output embeddings as the visual symbols. Finally, a Dynamic Logic Tensor Network (D-LTN) stepped up as the rule verifier to deliver the final output.
</p>

<p align="center">
 <img src="readme_files/functional.png" width="500px">
</p>

<p align="justify">
 While this functional setup might look simplistic at the first look, the D-LTN was the <i>real</i> challenge of my work. In that module, I dynamically convert symbolic rules into LTNs, which required building a parser for FOL and crafting an autonomous pipeline to train and test those D-LTNs. To make that happen, I used <a href="https://lark-parser.readthedocs.io/en/stable/">Lark</a> and sprinkled in some <i>meta-programming</i> magic to create a Python template that reads and understands FOL as a logic-loving compiler. This pipeline is the secret sauce, letting the system hum along smoothly while keeping those flexibility, explainability, and formality promises.

## The Codes

<p align="justify">
  Finally, it's time to roll up our sleeves and get into the real business. I've prepared a minimalistic implementation of this project in the repository. You could clone it locally or spin it up in the cloud, but let's keep things simple: I've tuned the code to run smoothly on Google Colab, which means you'll need a bit of Google Drive space as well. To get started, create a folder in your Drive and name it whatever fancy name you like. Let's say you go with <code>nesy</code> and put it into your home folder like a sane person. Then, just drag and drop <a href="data_collection.ipynb">data_collection.ipynb</a>, <a href="main_algorithm.ipynb">main_algorithm.ipynb</a>, <a href="visudo_scripts.zip">visudo_scripts.zip</a>, and <a href="prepared_datasets">prepared_datasets</a> into your <code>nesy</code> folder. That's it, you're ready to run the show.
</p>

<p>
 Just a quick heads-up about <a href="visudo_scripts.zip">visudo_scripts.zip</a>. I pulled these scripts from the <a href="https://github.com/linqs/visual-sudoku-puzzle-classification">original repository</a> behind the Sudoku task. So, the datasets aren't my artwork; they're collected using the exact same method described in their paper and repository. That's actually why I keep saying <q>collect</q> instead of <q>generate</q>. If you want the full scoop on this project, definitely check out that original repository.
</p>

### Data Collection

<p align="justify">
 The notebook <a href="data_collection.ipynb">data_collection.ipynb</a> handles collecting the data for the Sudoku task. If you're feeling lazy (no judgment), you can skip this entirely. The datasets you need are already collected in <a href="prepared_datasets">prepared_datasets</a>. But if you're the curious type who wants to know how I did it or roll your own, here's the lowdown. I tried to make the code self-explanatory, but here are the key bits:
 
 <ul>
  
  <li><b>Setting up constants</b>: In the <code>Notebook Initialization</code> section, you'll spot two crucial constants. First, <code>DRIVE_ROOT_DIR_PATH</code> stores the path to your <code>nesy</code> folder (for me, it was <code>'MyDrive/nesy'</code>). Second, <code>DRIVE_DATASETS_DIR</code> names the subfolder inside your <code>nesy</code> folder where your collected datasets live (I set it by default to <code>'prepared_datasets'</code>). Again: I've already run this beast for hours and gathered everything you need, which it's tucked away in <a href="prepared_datasets">prepared_datasets</a>. But to avoid chaos, you could tweak <code>DRIVE_DATASET_DIR</code> and collect your own fresh batch.</li>
  
  <li><b>Dataset collection and visualization</b>: Scroll down to the <code>Collection</code> subsection under the <code>Data Collection</code> section, where you'll find two functions: <code>collect</code> and <code>visualize</code>. Their names are pretty self-explanatory. The magic happens in their arguments: use <code>source_name</code> to pick the digit style for your Sudoku boards (I ran the code for <code>'MNIST'</code>, <code>'EMNIST'</code>, <code>'FMNIST'</code>, and <code>'KMNIST'</code>); set <code>board_dim</code> for the board size (for it was always <code>4</code>); and choose <code>split</code> as the data division you want to collect (I set it to <code>1</code> to <code>11</code>). Check out the <a href="https://github.com/linqs/visual-sudoku-puzzle-classification">original repository</a> to know more about these settings.</li>
  
  <li><b>Transferring datasets to Google Drive</b>: At the end of the notebook, there's a little cell that zips everything up and ships your datasets to the folder you specified its name by setting <code>DRIVE_DATASETS_DIR</code>. Run it, and keep calm.</li>
 
 </ul>
 
</p>

### Main Algorithm
<p align="justify">
 The notebook <a href="main_algorithm.ipynb">main_algorithm.ipynb</a> contains the beating heart of the entire system. This code's also self-explanatory, but here are the most important notes:
 
 <ul>
  
  <li><b>Setting up constants</b>: In the <code>Notebook Initialization</code> section, you'll again find some constants. Except for <code>DRIVE_ROOT_DIR_PATH</code> and <code>DRIVE_DATASETS_DIR</code> which are the same as before, you also have two others. The first one, <code>DRIVE_LOGS_DIR</code is another subfolder in your <code>nesy</code> folder that stores the logs of your experiments. Feel free to rename it for different experiments. The other cosntant, <code>GROQ_API_KEY</code>, holds the API key from <a href="https://groq.com">groq.com</a>, which gives you free inference access to open-source VLMs.</li>
   
   <li><b>D-LTN</b>: The <code>D-LTN</code> section is the symbolic powerhouse of the system, where I define an FOL grammar for parsing logic statements, create classes for different LTN building blocks, and build a dynamic converter that turns FOL into D-LTNs. Don't worry if it looks like hieroglyphics right now; this part requires a solid NeSy and LTN background to truly appreciate. Once you're fluent, you'll find this section quite straightforward.</li>
   
   <li><b>CNN</b>: In the <code>Groundings Tools</code> subsection under the <code>Main Algorithms</code> section, you'll find the <code>EncoderNet</code> class, which is the humble CNN I mentioned earlier that forms the neural workhorse of the system.</li>
   
   <li><b>Main Function</b>: In the <code>Operation Tools</code> subsection under the <code>Main Algorithms</code> section, there's a very import function, called <code>main</code>. This function takes a dataset, an FOL statement, and a bunch of other arguments with descriptive names, then performs a single iteration of the system.</li>

   <li><b>Hyper-Parameter Tuning</b>: The  <code>Hyperparameter Tuning</code> subsection under the <code>Main Algorithms</code> section is where we tune the CNN. Any time you run this cell, new logs will be pushed in the folder you specified its name by setting <code>DRIVE_LOGS_DIR</code>.</li>

   <li><b>Rule Generation</b>: The <code>Rule Generation</code> subsection under the <code>Main Algorithms</code> section implements the main system loop I described earlier. If you've nailed all the previous steps, you'll be able to see how the system can successfully generate the rules of Sudoku in FOL. The results of this part are also logged.</li>

   <li><b>Experimental Tests</b>: The <code>Experimental Tests</code> subsection under the <code>Main Algorithms</code> section lets you put the generated FOL statements (or your own custom ones) under microscope. This is where CNN and D-LTN are joined to enable comparison against current methods in the literature. All results get logged, because in science, bragging rights come with receipts.</li>

 </ul>
</p>

## Outcome

### Hyper-Parameter tuning

### Rule Generation

### Comparison to State-of-the-Art

## Acknowledgement
<p align="justify">
 I'd like to express my deepest gratitude to my advisor, <a href="https://www.polito.it/personale?p=lia.morra">Professor Lia Morra</a>, for her continuous guidance, support, and encouragement throughout this research. I'm also thankful to the members of her team, especially Ph.D candidate <a hre="https://www.polito.it/personale?p=alessandro.russo">Alessandro Russo</a>, for his valuable feedback.
</p>
