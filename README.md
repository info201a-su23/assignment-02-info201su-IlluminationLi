# Assignment 2: Protests

In recent years the United States has experienced a surge of protests, in support of Black Lives Matter, gender equity, and many other social or political issues.

In this assignment, you will work with data from [Count Love](https://countlove.org/), data that is ocassionally [cited](https://www.nytimes.com/2020/08/28/us/black-lives-matter-protest.html) by the *New York Times* when reporting on US demonstrations.

Through this assignment, you will be able to answer questions about protests, including:

-   What were the most attended and least attended protests in the US in the last 5 years?
-   How many protests occurred in Washington state?
-   How did the number of protests in 2019 compare to 2020, and why?
-   Why are people protesting in the US? What are the biggest motivators?

## Learning objectives

By completing the assignment, you will develop or skills for:

-   **Version control** tools for managing code (git and GitHub)
-   Writing documents with **markdown** syntax
-   Coding in R
-   Thinking critcally about data.

# 1. Critical Analysis & Reflection: Before You Code

Before diving into this (or any) dataset, it's important to know where the data came from, and it's important to have or to seek out *domain familiarity* --- that is, knowledge about the topic of the dataset. Sometimes the topic is very narrow; more often it is expansive, as in the case of CountLove. We don't want to be "strangers in the dataset," as Catherine D'Ignazio and Lauren Klein describe it. To get more familiar, we are going to begin by doing some background reading.

**Note:** Please write your answers below under the heading "Your Responses and Reflections."

-   First, please read [this FAQ](https://countlove.org/faq.html) from the CountLove website and the opening of [this blog post](https://www.tommyleung.com/countLove/index.htm). **(R1a)** Based on the information in these pieces, why did the creators start collecting the CountLove data?

-   Next, we would like you to read this [New York Times piece that uses CountLove data](https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html) and that describes the Black Lives Matter protests that occurred in the summer of 2020. **(R1b)** Please summarize the main point or argument of this article.

Next, we're going to reflect about who collected this data, and what's actually inside it.

**(R1c)** Who collected and shared the CountLove data, and what do they do for a living?

**(R1d)** As Klein and D'Ignazio remind us, when it comes to data, "what gets counted counts." What types of demonstrations does CountLove include in their data, and what types do they exclude?

**(R1e)** How and where does CountLove get their data about the protests?

**(R1f)** How does CountLove make their estimates about the number of people who attended a protest? What potential problems might arise from this method of estimation?

**(R1g)** What are two central values of Count Love? Name and briefly describe them. (See the Envisioning Cards for a defintion of "value".)

**(R1h)** Name and briefly describe one direct stakeholder and one indirect stakeholder (See the Envisioning Cards)?

# 2. Coding in R: Parts 1-6

**Instructions**. Assignment instructions and prompts are in this file: [analysis.R](analysis.R).

**Coding and reflection prompts**. You will find two kinds of prompts in [analysis.R](analysis.R):

-   *Coding prompts*, which prompt you to write R code in [analysis.R](analysis.R).
-   *Reflection prompts*, which prompt you to think and write in English below, in this file (README.md).

**Formatting Your Responses and Reflections**.

-   When formatting your written responses and reflections below, please *retain* all reflection prompt IDs (e.g., R1a, R2a, etc.).
-   Fill in the elipses (...) with your own words.
-   Remove expected word counts.
-   To write clearly, use markdown code appropriately (e.g., **bold**, *italics*, and `code`). As appropriate, include images, links, and so forth.

**Questions?** As always, please post on Teams or ask your Instructor or Teaching Assistant.

:computer: Good coding! :writing_hand: Good critical thinking! :smile: Good-luck!

(*Updated: October 2022, Your Teaching Team*)

# 3. Critical Analysis & Reflection: After You Code

In the second chapter of *Data Feminism*, Klein and D'Ignazio describe 4 ways that data scientists can challenge power and take action: \> Taking action can itself take many forms, and in this chapter we offer four starting points:\
\> (1) Collect: Compiling counterdata---in the face of missing data or institutional neglect---offers a powerful starting point as we see in the example of the DGEI, or in María Salguero's femicide maps discussed in chapter 1.\
\> (2) Analyze: Challenging power often requires demonstrating inequitable outcomes across groups, and new computational methods are being developed to audit opaque algorithms and hold institutions accountable.\
\> (3) Imagine: We cannot only focus on inequitable outcomes, because then we will never get to the root cause of injustice. In order to truly dismantle power, we have to imagine our end point not as "fairness," but as co-liberation.\
\> (4) Teach: The identities of data scientists matter, so how might we engage and empower newcomers to the field in order to shift the demographics and cultivate the next generation of data feminists?

**(R1h)** How does the CountLove project embody one or more of these 4 forms of challenging power?

**(R1i)** What is the most interesting or surprising thing you learned from this analysis? Please answer in at least 2-3 sentences (2 points)

**(R1j)** What is a kind of analysis that you would like to do or that would be interesting to do with the CountLove data that you don't have the time or skills to accomplish at this moment? Please answer in at least 2-3 sentences (2 points)

## Your Responses and Reflections

### Critical Analysis & Reflection: Before You Code (questions above)

-   **(R1a)** The creators started to collect the CountLove data to keep the records of ongoing protests (such as where, when, people participated...). They make these data more accessible for the general public. As it mentioned on their websites - "We hope that keeping a factual record of ongoing demonstrations and making this data more accessible helps citizens, journalists, and politicians make more compelling cases for a diverse, empathetic, and kind country."
-   **(R1b)** The article tried to show how the BLM movement was going in different state in the United States and its importance for people in different area.
-   **(R1c)** They are Tommy Leung and Nathan Perkins, engineers and scientists with a keen interest in civic responsibility and public policy.
-   **(R1d)** Included: public displays of protest that aren't part of "regular business", focusing on demonstrations that express dissent and demand change; Excluded: awareness events, commemorative celebrations, historic reenactments, fundraising events, town halls, or political campaign rallies
-   **(R1e)** Where: through local newspaper and television sites on a daily basis; How: these data is extracted through their software that can aggregate and visualize it.
-   **(R1f)** How to estimate: they record the most conservative attendance number mentioned in news articles, interpreting "a dozen" as 10, "dozens" as 20, "hundreds" as 100, and so on; Potential problem: less precision and accuracy because of the wide range they interpreted.
-   **(R1g)** * Accessibility: they well-organize the data and make it accessible to journalists and citizens quickly and clearly. * Factual record (real data): keep the data accurate and comprehensive. Be real, No manipulation, No exaggeration.
-   **(R1h)** * Direct stakeholder: Journalists and media that need data to show something. For example: Crowd Counting Consortium (CCC). * Indirect stakeholder: the general public that just want to know news or to benefit from accessible and reliable protest data to engage in ongoing events.

### Part 3: Locations (`analysis.R`)

-   **(R3a)** Not surprised. Part of the reason is that Washington is a big state with dense population. I went to the Strike protest last quarter with my friends (the one just after the spring quarter). We live in a world that our voice can be heard and be respected.
-   **(R3b)** I find that using sapply() function is a very efficient. I believe there must be other functions similar to sapply() that can deal with larger vectors and data in math. Feel excited to learn more about it.
-   **(R3c)** There are still some problems data missing, outliers and human-made errors. (for example, WA and wA). I'm wondering maybe we can use AI to check common error before we analysis the data, which may increase our efficiency.

### Critical Analysis & Reflection: After You Code (questions above)

-   **(R7h)** The CountLove project is incredible because it challenges the lack of LGBTQ+ representation in media. By involving overlooked individuals, it can gather important insights and give a platform to marginalized voices. This shows the power of data for change and a more inclusive society just like what we as students want to achieve in the future. CountLove embodies "collect" and "teach" by compiling protest data and making it accessible for everyone. It also embraces "teach" by making its data easily accessible for use, supporting the education of the next generation of data analysts and empowering those who wants to gain some knowledge. I believe that data can be a potent tool for driving change. By adopting a people-centered approach and unleashing creativity, we can use data to create a significant impact.

-   **(R7i)** In the assignment,I learnt what the CountLove project is all about and its importance to our world. Also, I improved data sorting and learned to use functions in R effectively. Practical exercises highlighted data manipulation's importance and how functions make code better. The assignment laid a strong foundation for data handling and showed data's power. I'm looking for how to apply these skills in different areas as I continue my data analysis journey in the future. I believe I will learn more thing that is interesting to me.
-   **(R7j)** I aimed to explore the correlation between the demographics and the frequency of the protest in the areas. It seems reasonable to link these two variables and to see their covariance. By identifying common patterns in these activities across different regions happening simultaneously, we can gain valuable insights into the issues that truly concern people.
