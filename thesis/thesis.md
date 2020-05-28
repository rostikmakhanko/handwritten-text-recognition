---


---

<h1 id="welcome-to-stackedit">Welcome to StackEdit!</h1>
<p>Hi! I’m your first Markdown file in <strong>StackEdit</strong>. If you want to learn about StackEdit, you can read me. If you want to play with Markdown, you can edit me. Once you have finished with me, you can create new files by opening the <strong>file explorer</strong> on the left corner of the navigation bar.</p>
<p>I’m gonna write my thesis.</p>
<h1 id="introduction">Introduction</h1>
<p>First of all let’s look at a problem of handwritten text recognition without any particular connections to technologies. In ancient times people used to paint animals or nature signs on the walls of caves to save notifications to other people. Then they realized that a better idea is to use some determined list of symbols. …</p>
<h1 id="thesis-roadmap">Thesis roadmap</h1>
<p><em>Based on <a href="https://medium.com/swlh/12-steps-to-applied-ai-2fdad7fdcdf3">Cassie Kozyrkov’s 12 Steps to Applied AI</a></em></p>
<p><img src="https://miro.medium.com/max/1400/1*DWpwjk-yqNliqQlkqBKfUw.jpeg" alt="alt text"></p>
<ol start="0">
<li>
<p>Reality check(is this problem exists, needs, and could to be solved).</p>
</li>
<li>
<p>Define what is success for my project.</p>
</li>
<li>
<p>Get data. Research for exists data sets. Decide how it could be improved.</p>
</li>
<li>
<p>Split data into three datasets: training, validation, and test.</p>
</li>
<li>
<p>Analyze part of the data with some plots. Make changes based on the analysis. Choose algorithms and models.</p>
</li>
<li>
<p>Prepare machine learning tools. Transform data into an appropriate format.</p>
</li>
<li>
<p>Use tools to train models.</p>
</li>
<li>
<p>Debug, analyze, and tune prepared data and models. Try to find what’s going wrong.</p>
</li>
<li>
<p>Validate models(does it works for the data).</p>
</li>
<li>
<p>Test the model. The moment where <a href="https://towardsdatascience.com/statistics-for-people-in-a-hurry-a9613c0ed0b">statistics</a> comes.</p>
</li>
<li>
<p>Build a system(UI or API) and integrate models in it.</p>
</li>
<li>
<p>Test what was built so far. Launch on servers or build setups.</p>
</li>
<li>
<p>Give to users(relatives, friends, teachers).</p>
</li>
</ol>
<h1 id="key-terminology">Key terminology</h1>
<p>In a nutshell, machine learning is the labeling of things. We get some data on input(it could be nearly anything - numbers, text, photo, sound), and our task to put a label on this data.</p>
<p>Let’s start with the task easier than a recognition of a large handwritten text - recognition of letters(a, b,…, z). Input is a photo of one of the letters and the computer needs to provide an output, which letter is on a photo. On this example we use these terms:</p>
<ul>
<li><strong>Feature</strong> <code>x</code> is an input, photo of a handwritten letter. In larger machine learning projects could be a lot of different features that marked as <code>[x_1,x_2,...,x_n]</code>.</li>
<li><strong>Label</strong> <code>y</code> is a thing that we are predicting, it could be one of the values <code>['a', 'b',..., 'z']</code>.</li>
<li><strong>Example</strong> is a particular instance of data, <code>x</code>. Important that <code>x</code> isn’t necessarily single value, so talking about <code>x</code> we mean multi-dimension vector. In our case <code>x</code> is a photo, that could be represented as a matrix of pixels. An example could be labeled or unlabeled. Labeled example includes both feature(s) and the label: <code>{x, y} = {file('letter_r.jpg'), 'r'}</code></li>
<li><strong>Model</strong> defines the relationship between feature and label. It finds the correct label for the input photo. The process of <strong>training</strong> means learning the model of this relationship by labeled examples. <strong>Inference</strong> is the process of applying the model to unlabeled data.</li>
<li>For the example we need to train <strong>classification model</strong> because the task is to answer which letter from the set <code>['a', 'b',..., 'z']</code> is on a photo, classify input photo.</li>
</ul>
<h1 id="training-and-test-sets">Training and test sets</h1>
<p>After searching dataset it’s important to split it into two:</p>
<ul>
<li><strong>Training set</strong> is a subset to train a model,</li>
<li><strong>Test set</strong> is a subset to evaluate the success of the trained model.</li>
</ul>
<p>The test set might be 10 times smaller than the Training set, but we need to make sure that the overall dataset is large enough.</p>
<p>There are two important issues. First is to <strong>randomize dataset</strong> before splitting it into training and test sets. And, second is to <strong>never train a model on test set</strong>.</p>
<h1 id="stages-of-product-development">Stages of product development</h1>
<ol>
<li>
<p><strong>Arabic numerals</strong> recognition <code>['0', '1',..., '9']</code>(<a href="http://yann.lecun.com/exdb/mnist/">MNIST</a>).</p>
</li>
<li>
<p><strong>English alphabet letters</strong> recognition <code>['a', 'b',..., 'z']</code>.</p>
</li>
<li>
<p><strong>Client version of 1. or 2.</strong> for browser or mobile.</p>
</li>
<li>
<p>Merge 1. and 2. for <strong>letters and numbers sequences</strong> recognition.</p>
</li>
<li>
<p><strong>Client version of 4.</strong> for browser or mobile.</p>
</li>
<li>
<p><strong>Handwritten English words</strong> recognition.</p>
</li>
<li>
<p>Improve <strong>7. with reinforcements</strong> like a set of expected words.</p>
</li>
<li>
<p><strong>Client version of 7.</strong> for browser or mobile.</p>
</li>
<li>
<p>Recognition of <strong>handwritten English text</strong>.</p>
</li>
<li>
<p><strong>Client version of 9.</strong> (could work along with some Cloud-based computations).</p>
</li>
<li>
<p><em>Bonus</em>: Recognition of <strong>Ukrainian alphabet letters</strong>.</p>
</li>
</ol>
<h1 id="objects-detection">Objects detection</h1>
<p>Object detection is a computer technology related to computer vision and image processing that deals with detecting instances of semantic objects of a certain class (such as humans, buildings, or cars) in digital images and videos. Well-researched domains of object detection include face detection and pedestrian detection. Object detection has applications in many areas of computer vision, including image retrieval and video surveillance. <a href="https://en.wikipedia.org/wiki/Object_detection">Wikipedia</a></p>
<p>Large technological companies such as Google, Amazon, IBM etc., and starups such as <a href="http://Scale.ai">Scale.ai</a> and Immage provide their high-quality cloud-based APIs.</p>

