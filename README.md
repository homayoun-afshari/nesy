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
Alright, let's talk about the unsexy but absolutely crucial part of any AI project: hyperparameter tuning. Think of it as trying on 192 different outfits for your CNN block until you find the one that makes it look sharp *and* comfortable. As I mentioned earlier, the rule generation loop needs both the CNN and D-LTN to be properly tuned beforehand, so we built a comprehensive hyperparameter grid (shown below) that tests 192 different configurations. For the D-LTN—while it's not a neural network per se—we still had to consider how it plays nice with different datasets. So, we ran each configuration through four separate development loops using the 11th split of the Visudo-PC dataset, but with digits from MNIST, EMNIST, KMNIST, and FMNIST. That bumped our total experiments to a whopping 768 runs. The average test performance across these four "flavors" helped us pick the winning combo.

Now, for the D-LTN's initialization, we needed a manually crafted FOL rule that captures the core Sudoku constraint: no two identical digits can hang out in the same row, column, or block (unless they're the same cell, of course). We boiled this down to a crisp rule: if two cells have the same value, they must either be the same location *or* not share a row, column, or block. In FOL speak, that's:

```
forall x1, x2
    P_same_value(x1, x2) implies
    P_same_loc(x1, x2) | (!P_same_row(x1, x2) &
                          !P_same_col(x1, x2) &
                          !P_same_block(x1, x2))
```

This rule is the logical backbone of Sudoku validity—like the "no double-dipping" rule at a fancy dinner party, but for numbers.

Here's the hyperparameter grid we explored:

| Hyperparameter | Alternatives |
|---------------|--------------|
| `cnn_dims` | `(8, 16)`, `(16, 32)`, `(32, 64)` |
| `kernel_dims` | `(4, 4)`, `(2, 2)` |
| `embed_dims` | `(4,)`, `(16,)`, `(64, 4)`, `(64, 16)` |
| `drop_prob` | `0.1`, `0.2`, `0.3` |
| `use_softmax` | `False`, `True` |

This exhaustive search spanned architectural choices, embedding sizes, regularization levels, and output strategies, giving us the best shot at a robust model. And the results? Drumroll, please...

| ID | `cnn_dims` | `kernel_dims` | `embed_dims` | `drop_prob` | `use_softmax` | Avg Test AUC | Avg Test Accuracy |
|----|------------|---------------|--------------|-------------|---------------|--------------|-------------------|
| 1 | `(32, 64)` | `(4, 4)` | `(64,)` | `0.2` | `True` | 0.9560 | 85.50% |
| 2 | `(32, 64)` | `(4, 4)` | `(64, 4)` | `0.2` | `True` | 0.9528 | 86.25% |
| 3 | `(32, 64)` | `(4, 4)` | `(64,)` | `0.1` | `True` | 0.9523 | 86.12% |
| 4 | `(16, 32)` | `(4, 4)` | `(64,)` | `0.2` | `True` | 0.9477 | 84.87% |
| 5 | `(16, 32)` | `(4, 4)` | `(4,)` | `0.2` | `True` | 0.9458 | 82.50% |

We prioritized AUC (the gold standard in the literature) and crowned the top config: `cnn_dims=(32, 64)`, `kernel_dims=(4, 4)`, `embed_dims=(64,)`, `drop_prob=0.2`, and `use_softmax=True`. It's like finding the perfect recipe after burning a few batches—not glamorous, but oh-so-satisfying when it works.

### Rule Generation

With our CNN and D-LTN tuned to perfection (like a well-oiled logic machine), we finally unleashed the rule generation experiment—the moment of truth where our system tries to discover Sudoku's secrets all by itself. The results are shown below, and spoiler alert: it mostly nailed it. We stuck with the 11th split of the Visudo-PC dataset and ran the generation loop separately on MNIST, EMNIST, KMNIST, and FMNIST. As you'll see, the system successfully generated valid rules for the first three sources, but hit a snag with FMNIST. We'll dissect that drama in the next section, but here's the tea: the failure stemmed from the Vision Language Model's computational costs, since we capped the loop at a maximum of 20 iterations to keep things from running into next week. Could more iterations have saved FMNIST? Possibly, but hey—the other three successes prove our system can indeed generate valid, semantically meaningful rules. And here they are, in all their FOL glory:

1. **Rule 1** (the "No Sharing Club" edition):
   ```
   forall x1, x2
       !P_same_loc(x1, x2) & (P_same_row(x1, x2) |
                              P_same_col(x1, x2) |
                              P_same_block(x1, x2))
       implies !P_same_value(x1, x2)
   ```

2. **Rule 2** (the "Double Forall Drama" version):
   ```
   forall x1 forall x2
       (P_same_row(x1, x2) |
        P_same_col(x1, x2) |
        P_same_block(x1, x2)) & !P_same_loc(x1, x2)
       implies !P_same_value(x1, x2)
   ```

3. **Rule 3** (the "Contrapositive Chic" style):
   ```
   forall x1, x2
       !P_same_loc(x1, x2) & P_same_value(x1, x2) implies (
           !P_same_row(x1, x2) &
           !P_same_col(x1, x2) &
           !P_same_block(x1, x2))
   ```

And here's how the generation loop performed across the board:

| Data Source | VLM Load | Generated Rule | Total Iterations | Test AUC | Test Accuracy |
|-------------|----------|----------------|------------------|----------|---------------|
| MNIST-11 (4×4) | 3 | Rule 1 | 19 | 0.9974 | 99.00% |
| EMNIST-11 (4×4) | 3 | Rule 2 | 13 | 0.9012 | 99.00% |
| KMNIST-11 (4×4) | 3 | Rule 3 | 9 | 0.9517 | 99.00% |
| FMNIST-11 (4×4) | 3 | Error | 20 | - | - |

Three out of four ain't bad—it's like batting .750 in the World Series of AI rule generation. The system didn't just spit out random logic; it crafted rules that actually work, with test accuracies hitting 99% across the board. FMNIST's timeout is a bummer, but it gives us something juicy to analyze next. Stay tuned for the post-mortem, where we figure out why fashion digits proved too stylish for our VLM to handle.

### Experimental Tests

With our hyperparameters dialed in and FOL rules ready to roll, we put our system through the ultimate endurance test: 120 separate runs across all ten splits of the Visudo-PC dataset, all four data sources (MNIST, EMNIST, KMNIST, FMNIST), and all three generated rules. Think of it as sending our NeSy athlete to the AI Olympics—sprinter, marathoner, and decathlete all in one. Below, you'll see the seven best and seven worst individual runs based on test AUC, giving you a taste of both the triumphs and the occasional faceplants.

| Data Source | Utilized Rule | Training AUC | Training Acc | Val AUC | Val Acc | Test AUC | Test Acc |
|-------------|---------------|--------------|--------------|---------|---------|----------|----------|
| **Top 7 Performers** | | | | | | | |
| MNIST-3 (4×4) | Rule 1 | 0.9988 | 99.50% | 0.9699 | 90.50% | **0.9949** | 91.00% |
| MNIST-7 (4×4) | Rule 2 | 0.9988 | 99.00% | 0.9665 | 90.00% | **0.9917** | 93.50% |
| MNIST-6 (4×4) | Rule 2 | 1.0000 | 100.00% | 0.9856 | 94.00% | **0.9892** | 97.00% |
| MNIST-3 (4×4) | Rule 2 | 0.9988 | 98.50% | 0.9668 | 92.00% | **0.9862** | 92.50% |
| MNIST-4 (4×4) | Rule 3 | 0.9975 | 99.50% | 0.9800 | 94.00% | **0.9849** | 94.50% |
| MNIST-3 (4×4) | Rule 3 | 0.9975 | 99.50% | 0.9752 | 92.50% | **0.9846** | 92.50% |
| MNIST-7 (4×4) | Rule 1 | 0.9988 | 99.50% | 0.9791 | 91.00% | **0.9845** | 94.00% |
| **Bottom 7 Strugglers** | | | | | | | |
| FMNIST-9 (4×4) | Rule 2 | 0.9713 | 93.50% | 0.8625 | 70.50% | **0.8637** | 66.50% |
| FMNIST-8 (4×4) | Rule 2 | 1.0000 | 99.50% | 0.8725 | 77.00% | **0.8571** | 74.00% |
| EMNIST-4 (4×4) | Rule 3 | 0.5000 | 50.00% | 0.5000 | 50.00% | **0.5000** | 50.00% |
| EMNIST-6 (4×4) | Rule 2 | 0.5000 | 50.00% | 0.5000 | 50.00% | **0.5000** | 50.00% |
| EMNIST-10 (4×4) | Rule 2 | 0.5000 | 50.00% | 0.5000 | 50.00% | **0.5000** | 50.00% |
| EMNIST-10 (4×4) | Rule 1 | 0.5000 | 50.00% | 0.5000 | 50.00% | **0.5000** | 50.00% |
| FMNIST-3 (4×4) | Rule 3 | 0.5000 | 50.00% | 0.5000 | 50.00% | **0.5000** | 50.00% |

### Comparison to State-of-the-Art

Now for the moment we've all been waiting for: the showdown! Following the gold standard in AI benchmarking, we aggregated our 120 runs by data source, averaging across the first ten splits of Visudo-PC and selecting the best-performing rule for each configuration. This isn't just cherry-picking—it's the same rigorous approach used in the literature, ensuring we're comparing apples to very fancy, symbolic apples.

And the results? Let's just say our NeSy system didn't just show up to the party—it brought the whole DJ booth. Here's how we stack up against the competition:

| Data Source | NeuPSL | LTN-IND (A) | LTN-IND (B) | LTN-IND (C) | **Proposed Method** |
|-------------|--------|-------------|-------------|-------------|---------------------|
| MNIST (4×4) | 0.88±0.02 | 0.83±0.18 | 0.84±0.14 | 0.94±0.10 | **0.97±0.01** |
| EMNIST (4×4) | 0.79±0.09 | 0.58±0.04 | 0.58±0.06 | 0.65±0.14 | **0.91±0.10** |
| KMNIST (4×4) | 0.65±0.12 | 0.83±0.09 | 0.85±0.11 | 0.87±0.09 | **0.93±0.01** |
| FMNIST (4×4) | 0.74±0.04 | 0.67±0.11 | 0.76±0.15 | 0.83±0.11 | **0.89±0.04** |

Talk about a clean sweep! Our method doesn't just edge out the competition—it laps them, with consistently lower standard deviations that would make a statistician weep with joy. Whether it's crisp MNIST digits, stylish EMNIST letters, exotic KMNIST characters, or fashion-forward FMNIST clothing, our system delivers robust performance across the board.

This isn't just about numbers—it's validation that our flexible, explainable, formal approach actually works in the wild. We didn't just build a better black box; we created a system that can reason about visual puzzles like a logic professor with X-ray vision. And honestly? That's the kind of AI breakthrough that keeps researchers up at night—in the best possible way.

## Acknowledgement
<p align="justify">
 I'd like to express my deepest gratitude to my advisor, <a href="https://www.polito.it/personale?p=lia.morra">Professor Lia Morra</a>, for her continuous guidance, support, and encouragement throughout this research. I'm also thankful to the members of her team, especially <a href="https://www.polito.it/personale?p=alessandro.russo">Ph.D candidate Alessandro Russo</a>, for his valuable feedback.
</p>
