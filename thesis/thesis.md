# Welcome to StackEdit!

Hi! I'm your first Markdown file in **StackEdit**. If you want to learn about StackEdit, you can read me. If you want to play with Markdown, you can edit me. Once you have finished with me, you can create new files by opening the **file explorer** on the left corner of the navigation bar.

I'm gonna write my thesis.


# Introduction
First of all let's look at a problem of handwritten text recognition without any particular connections to technologies. In ancient times people used to paint animals or nature signs on the walls of caves to save notifications to other people. Then they realized that a better idea is to use some determined list of symbols. ...

# Thesis roadmap

*Based on [Cassie Kozyrkov's 12 Steps to Applied AI](https://medium.com/swlh/12-steps-to-applied-ai-2fdad7fdcdf3)*

![alt text](https://miro.medium.com/max/1400/1*DWpwjk-yqNliqQlkqBKfUw.jpeg)

0. Reality check(is this problem exists, needs, and could to be solved).

1. Define what is success for my project.

2. Get data. Research for exists data sets. Decide how it could be improved.

3. Split data into three datasets: training, validation, and test.

4. Analyze part of the data with some plots. Make changes based on the analysis. Choose algorithms and models.

5. Prepare machine learning tools. Transform data into an appropriate format.

6. Use tools to train models.

7. Debug, analyze, and tune prepared data and models. Try to find what's going wrong.

8. Validate models(does it works for the data).

9. Test the model. The moment where [statistics](https://towardsdatascience.com/statistics-for-people-in-a-hurry-a9613c0ed0b) comes.

10. Build a system(UI or API) and integrate models in it.

11. Test what was built so far. Launch on servers or build setups.

12. Give to users(relatives, friends, teachers).

# Key terminology
In a nutshell, machine learning is the labeling of things. We get some data on input(it could be nearly anything - numbers, text, photo, sound), and our task to put a label on this data.

Let's start with the task easier than a recognition of a large handwritten text - recognition of letters(a, b,..., z). Input is a photo of one of the letters and the computer needs to provide an output, which letter is on a photo. On this example we use these terms:

* **Feature** `x` is an input, photo of a handwritten letter. In larger machine learning projects could be a lot of different features that marked as `[x_1,x_2,...,x_n]`.
* **Label** `y` is a thing that we are predicting, it could be one of the values `['a', 'b',..., 'z']`.
* **Example** is a particular instance of data, `x`. Important that `x` isn't necessarily single value, so talking about `x` we mean multi-dimension vector. In our case `x` is a photo, that could be represented as a matrix of pixels. An example could be labeled or unlabeled. Labeled example includes both feature(s) and the label: `{x, y} = {file('letter_r.jpg'), 'r'}`
* **Model** defines the relationship between feature and label. It finds the correct label for the input photo. The process of **training** means learning the model of this relationship by labeled examples. **Inference** is the process of applying the model to unlabeled data.
* For the example we need to train **classification model** because the task is to answer which letter from the set `['a', 'b',..., 'z']` is on a photo, classify input photo.

# Training and test sets
After searching dataset it's important to split it into two:

* **Training set** is a subset to train a model,
* **Test set** is a subset to evaluate the success of the trained model.

The test set might be 10 times smaller than the Training set, but we need to make sure that the overall dataset is large enough.

There are two important issues. First is to **randomize dataset** before splitting it into training and test sets. And, second is to **never train a model on test set**.

# Stages of product development
1. **Arabic numerals** recognition `['0', '1',..., '9']`([MNIST](http://yann.lecun.com/exdb/mnist/)).

2. **English alphabet letters** recognition `['a', 'b',..., 'z']`.

3. **Client version of 1. or 2.** for browser or mobile.

4. Merge 1. and 2. for **letters and numbers sequences** recognition.

5. **Client version of 4.** for browser or mobile.

6. **Handwritten English words** recognition.

7. Improve **7. with reinforcements** like a set of expected words.

8. **Client version of 7.** for browser or mobile.

9. Recognition of **handwritten English text**.

10. **Client version of 9.** (could work along with some Cloud-based computations).

11. *Bonus*: Recognition of **Ukrainian alphabet letters**.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA5Nzg4MzU4N119
-->