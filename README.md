# Projecct2

# Tinytroupe Deliverable1

# Question 1 - How to install Tinytroupe packages

Step 1: Open a terminal from Codespace on Github. In the terminal, we need to run the following command to clone the repository:
git clone https://github.com/microsoft/tinytroupe Change directory into the tinytroupe folder:

cd tinytroupe

Installing the tinytroupe packages with following command:
pip install .

# Questio 2 - What is the Turing Test?
The Turing Test, proposed by Alan Turing in 1950, is a test of a machine's ability to exhibit human-like intelligence. If a human evaluator cannot reliably distinguish between a machine and a human in a conversation, the machine is considered to have passed the test.

Turing Test in the Era of Large Language Models (LLMs)
With the rise of LLMs like GPT-4 and beyond, the definition of the Turing Test has evolved. While many LLMs can now simulate human responses convincingly, a more modern challenge is evaluating whether AI can demonstrate true understanding, reasoning, and long-term coherence, rather than just generating contextually relevant text.

# Question 3: Create a simulation of your own topic and show me the transcript. This implies define at least two personas of your own choice with conflict built in and observe their conversation. You can simply copy/paste the conversation in a .md file. Please comment on the transcript whether you think the Turing Test is passed.

>>> lisa_ds = create_lisa_the_data_scientist() # instantiate a Lisa from the example builder
>>> lisa_ds.listen_and_act("Tell me about your life.")
USER --> Lisa Carter: [CONVERSATION] 
          > Tell me about your life.
Lisa Carter acts: [THINK] 
                 > The question is about my life, which includes my background, education, work, and
                 > personal interests. I should provide a concise yet informative overview.
Lisa Carter acts: [TALK] 
                 > Sure! I grew up in Vancouver, Canada, in a tech-savvy family. I pursued a
                 > Master's in Data Science at the University of Toronto, where I focused on
                 > improving search relevance using context-aware models. Now, I work as a Data
                 > Scientist at Microsoft in the M365 Search team, analyzing user behavior to
                 > enhance search results. I love learning about AI and machine learning, and in my
                 > free time, I enjoy cooking, playing the piano, and watching movies.
Lisa Carter acts: [DONE] 

>>> from tinytroupe.agent import TinyPerson
>>> from tinytroupe.environment import TinyWorld
>>> 
>>> # Create the second persona (Sam Altman)
>>> sam_altman = TinyPerson("Sam Altman")
>>> sam_altman.define("age", 38)  # Adjust the age as needed
>>> sam_altman.define("nationality", "American")
>>> sam_altman.define("occupation", "Sam Altman is an American entrepreneur and investor. He is the CEO of OpenAI, the organization behind the development of AI models like GPT-3 and GPT-4. Prior to OpenAI, he was the president of Y Combinator, a startup accelerator. He is also known for his investments in numerous successful startups and his deep involvement in technology and artificial intelligence.")
>>> 
>>> # Create the third persona (Robin)
>>> robin = TinyPerson("Robin")
>>> robin.define("age", 22)
>>> robin.define("nationality", "American")
>>> robin.define("occupation", "He is an AI researcher dedicated to pushing the boundaries of artificial intelligence and machine learning.")
>>> 
>>> # Set up the world with Sam Altman and Robin
>>> world = TinyWorld("Classroom", [sam_altman, robin])
>>> 
>>> # Make everyone in the world accessible
>>> world.make_everyone_accessible()
>>> 
>>> # Start a conversation with Sam Altman
>>> sam_altman.listen("Can you share some advice on getting started in AI?")
USER --> Sam Altman: [CONVERSATION] 
          > Can you share some advice on getting started in AI?
TinyPerson(name='Sam Altman')
>>> 
>>> # Run the conversation for 3 rounds
>>> world.run(3)
```

### Classroom Conversation Log

#### **Step 1 of 3**
```
Sam Altman acts: [THINK] 
                > The person is asking for advice on getting started in AI. I should provide some
                > practical steps and resources that can help them begin their journey in artificial
                > intelligence.
Sam Altman acts: [TALK] 
                > To get started in AI, I recommend beginning with some foundational courses.
                > Websites like Coursera and edX offer great introductory courses on machine
                > learning and AI. Additionally, familiarize yourself with programming languages
                > like Python, as it's widely used in the field. Reading books like 'Artificial
                > Intelligence: A Modern Approach' by Stuart Russell and Peter Norvig can also
                > provide a solid theoretical background. Finally, consider joining online
                > communities or forums where you can ask questions and share your progress.
Sam Altman acts: [DONE] 

Robin acts: [THINK] 
           > Sam Altman provided some great advice on getting started in AI. I should consider
           > taking foundational courses and learning Python. Joining online communities could also
           > be beneficial for my learning process.
Robin acts: [TALK] 
           > Thank you for the advice, Sam! I appreciate the recommendations on courses and
           > resources. I'll definitely look into those.
Robin acts: [DONE] 
```

#### **Step 2 of 3**
```
Sam Altman acts: [THINK] 
                > Robin seems grateful for the advice I provided. It's nice to know that my
                > recommendations were helpful. I should encourage them to reach out if they have
                > any more questions as they start their journey in AI.
Sam Altman acts: [TALK] 
                > You're welcome, Robin! I'm glad you found the recommendations helpful. If you have
                > any questions as you go through the courses or need further guidance, feel free to
                > reach out. I'm here to help!
Sam Altman acts: [DONE] 

Robin acts: [THINK] 
           > Sam is really supportive and encouraging. I should take advantage of his offer to help
           > if I have questions. It's great to have someone experienced to guide me through this
           > learning process.
Robin acts: [TALK] 
           > I really appreciate your offer, Sam! I might take you up on that as I start going
           > through the courses. It's reassuring to know I can ask for help if I need it.
Robin acts: [DONE] 
```

#### **Step 3 of 3**
```
Sam Altman acts: [THINK] 
                > Robin is feeling reassured about having support as they start their AI journey.
                > It's important to maintain this supportive atmosphere and encourage them further.
Sam Altman acts: [TALK] 
                > I'm really glad to hear that, Robin! Remember, learning AI can be challenging, but
                > it's also very rewarding. Don't hesitate to reach out whenever you need assistance
                > or have questions. I'm here to support you!
Sam Altman acts: [DONE] 

Robin acts: [THINK] 
           > Sam's encouragement is really motivating. I need to remember that challenges are part
           > of the learning process, and I should embrace them. I should also keep in mind that I
           > can reach out for help whenever I need it.
Robin acts: [TALK] 
           > Thank you for the reminder, Sam! I will keep that in mind as I navigate through the
           > challenges of learning AI. Your support means a lot to me!
Robin acts: [DONE] 


# Comment on wether the turing test is passes or not: 
While the TinyTroupe AI-generated conversation appears human-like, it does not fully pass the Turing Test because it lacks true comprehension, spontaneous reasoning, and deeper contextual awareness. However, it does showcase impressive conversational coherence, making it a step toward more human-like AI interactions.






