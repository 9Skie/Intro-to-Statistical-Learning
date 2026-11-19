Machine learning is about using data to learn patterns that help us make predictions, make decisions, or understand how things are organized.

This course introduces the methods that make that possible, along with ways to judge whether the patterns we learn are useful and reliable.


Consider recognizing a handwritten number. People write the same digit in many different ways: some people’s sevens have a line through them, some people’s ones have a little hook, and some people’s handwriting is barely readable. Yet we can usually recognize these digits because we have seen many examples.

![[Screenshot 2026-11-04 at 4.52.13 PM.jpg|500]]


A machine learning system learn from examples. We give it images of handwritten digits together with the correct answers. 

A learning algorithm uses those examples to build a **model**: a mathematical rule that connects an image to a predicted digit. Once trained, the model can receive a new image and predict what number it contains.

This introduces a distinction we will use throughout the course. 
- The **learning algorithm** is the procedure that learns from data. 
- The **model** is the resulting rule or representation. 
- **Training** is the process of using the data to fit or adjust that model.

Machine learning is one major approach within the broader field of **artificial intelligence**. **Statistical learning**, the subject of this course, overlaps heavily with machine learning. It places particular emphasis on learning relationships from data, understanding those relationships, and measuring the reliability of our conclusions.


## Supervised Learning

In supervised learning, the training examples include both the information available to us and the answer we want to predict. For handwritten digits, the information is an image and the answer is the digit.

The lecture calls the input information **X** and the outcome **Y**. 


A training example therefore connects an input to a known outcome:
- **Information about one example → its known answer**

The learning algorithm examines many such examples and finds a rule that can predict an answer from the available information. We then apply that rule to new cases whose answers we do not yet know.
- "Supervised" refers to the presence of these answers. 


Supervised learning includes two common kinds of prediction:

- **Regression predicts a numerical quantity**, such as a price or a temperature.
- **Classification predicts a category**, such as spam or legitimate email, house or bike.


Netflix has ratings that customers have given to movies, but each customer has rated only a small fraction of all available movies. The task is to use the observed ratings to predict ratings that are missing. Those predictions can help identify movies a customer might enjoy.

For intuition, imagine that two people have rated many of the same movies similarly. Their agreement might provide useful evidence about how one of them would rate a movie that only the other has rated.

Here are several applications that illustrate the kinds of tasks introduced in the course:

|Application|Information available|What we want to determine|
|---|---|---|
|Handwriting recognition|An image of handwritten digits|Which digits were written|
|Spam detection|Characteristics of an email|Whether it is spam|
|Medical classification|Measurements from a tissue sample|Which cancer category it belongs to|
|Numerical prediction|Relevant measurements about a person or object|A quantity such as blood pressure or price|
|Movie recommendations|Customers’ existing movie ratings|How a customer might rate another movie|

The applications differ, but they share a structure: use observations with known outcomes to learn something useful about cases whose outcomes are unknown.


## Unsupervised Learning

Sometimes we have data without a particular answer attached to each example. We might have measurements describing thousands of customers, for instance, without having decided which customer categories exist.

We can still ask whether the data contains useful structure. Perhaps some customers have similar purchasing patterns. Perhaps many measurements vary together, allowing us to describe the data using a smaller set of underlying patterns.

This is the central distinction between them.

|Supervised learning|Unsupervised learning|
|---|---|
|Training examples include a target answer, Y.|There is no supplied target answer for each example.|
|We learn to predict that answer from X.|We examine X to discover patterns or structure.|
|Typical tasks include regression and classification.|Typical tasks include clustering and finding compact representations of data.|

A form of unsupervised learning is clustering.
- **Clustering** means grouping observations according to their similarities. Another important technique, **principal component analysis**, finds a smaller set of combinations of measurements that captures much of the variation in the data.

They are two major categories covered in this class, though the broader field contains other learning settings. For example, reinforcement learning studies how an agent learns to choose actions from feedback about their consequences.

A central challenge throughout the course is determining whether a model has learned something that works beyond its training examples.

A model can fit the data it has already seen extremely well and still perform poorly on new cases. This happens when it captures accidental details or noise in the training data too closely, a problem called **overfitting**.
- That ability to work well on new cases is called **generalization**.


In practice, we use some data to train models, use separate data or carefully designed splits to choose between them, and reserve an independent evaluation for estimating final performance. The course develops ways to do this when data is limited.

**The course gradually develops the tools needed to build, compare, and understand these models.**


The main roadmap for Chapters 1–9 and 12 is:

|Chapter|Topic|Main idea|
|---|---|---|
|1–2|Introduction and statistical learning|Define learning problems, understand prediction, and assess model accuracy.|
|3|Linear regression|Predict a numerical outcome using a simple relationship between inputs and output.|
|4|Classification|Predict categories using methods such as logistic regression.|
|5|Resampling|Estimate performance and uncertainty through careful data splits and repeated sampling.|
|6|Model selection and regularization|Choose useful predictors and control model complexity.|
|7|Moving beyond linearity|Model relationships that bend or change shape.|
|8|Trees and related methods|Make predictions through sequences of decisions and combinations of many trees.|
|9|Support vector machines|Learn boundaries that separate categories.|
|12|Unsupervised learning|Discover groups and summarize structure in data without target answers.|

As you encounter each method, keep asking what data it needs, what it learns, how it produces a result, and how you can evaluate that result. Those questions will help you choose and use methods when you eventually face a dataset or problem that the instructors have never shown you.