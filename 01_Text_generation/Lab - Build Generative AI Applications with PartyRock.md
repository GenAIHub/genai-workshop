# AWS GenAI - Lab: Build Generative AI Applications with PartyRock

## What is PartyRock

In this lab, we'll learn how to use PartyRock to generate AI apps without any code. PartyRock is a shareable Generative AI app building playground that allows you to experiment with prompt engineering in a hands-on and fun way. In just a few clicks, you can build, share, and remix apps to get inspired while playing with Generative AI. For example, you can:

- Build an app to generate dad jokes on the topic of your choice.
- Create and play a virtual trivia game online with friends from around the world.
- Create an AI storyteller to guide your next fantasy roleplaying campaign.

By building and playing with PartyRock apps, you learn about the fundamental techniques and capabilities needed to get started with Generative AI, including understanding how a foundation model responds to a given prompt, experimenting with different text-based prompts, and chaining prompts together. Any builder can experiment with PartyRock by creating a profile using a social login from Amazon.com, Apple, or Google. PartyRock is separate from the AWS console and does not require an AWS account to get started.

## Exercise 1: Building a PartyRock Application

To highlight the power of PartyRock, we are going to build an application that can provide book recommendations based on your mood.

### Steps:
1. Head over to the [PartyRock website](https://partyrock.aws/).
2. Login with a social login from Amazon.com, Apple, or Google.
3. Click on "Build your own app."
4. Enter the following prompt: "Provide book recommendations based on your mood and a chat bot to talk about the books."
5. Click "Generate app."

### Using the App
PartyRock was able to create the interface needed to take in user input, provide recommendations, and create a chatbot just from your prompt. Now play around with the app by entering your mood and then asking the chatbot for more information about the book. 
Try entering "Happy". Afterwards, you can ask the chatbot, "Can you tell more about one of the books that was listed?" You can also share your app by clicking the "Make public and Share" button.

## Updating Your App

In PartyRock, each UI element is a *Widget* which displays content, takes in input, connects to other widgets, and creates output. Widgets that take in input allow users to interact with the app. Widgets that create output use prompts and references to other widgets to generate something like an image or text.

### Types of Widgets

There are 3 different types of AI-powered widgets:
1. Image generation
2. Chatbot
3. Text generation

You can edit AI-powered widgets to connect them to other widgets and make their output change.

There are also 2 other widgets:
1. User input
2. Static text

The user input widget allows users to change output when you connect it to AI-powered widgets. The static text widget provides a place for text descriptions. For more details, check out the [PartyRock Guide](https://partyrock.aws/guide/building).

## Exercise 2: Prompt Engineering Techniques

Create an app on PartyRock that validates prompt engineering techniques and displays results based on prompts from four different models.

### Steps:
1. Navigate to the PartyRock dashboard and click on "Generate App."
2. Name your app "Prompt Engineering Validator."
3. Add a description: "Create an app that validates prompt engineering techniques by displaying results from four different AI models: Anthropic Claude Sonnet, Amazon Titan Text, AI21Labs – Jurassic-2 Ultra, Llama 2 Chat 70B."

### Create Widgets:
- **User Input Widget:**
  - Add a "User Input" widget for the user to enter their prompt.
  - Title: "Enter Your Prompt."
- **AI-Powered Text Generation Widgets:**
  - Create four text generation widgets, each connected to a different model.
  - **Widget 1: Claude Sonnet**
    - Title: "Claude Response"
    - Model: Claude Sonnet
    - Prompt: Use the user input prompt by referencing the User Input widget with `@Enter Your Prompt`
    - Example: `@Enter Your Prompt`
  - **Widget 2: Amazon Titan**
    - Title: "Amazon Titan Response"
    - Model: Titan Text
    - Prompt: Use the user input prompt by referencing the User Input widget with `@Enter Your Prompt`
    - Example: `@Enter Your Prompt`
  - **Widget 3: AI21Labs**
    - Title: "AI21Labs Response"
    - Model: AI21Labs
    - Prompt: Use the user input prompt by referencing the User Input widget with `@Enter Your Prompt`
    - Example: `@Enter Your Prompt`
  - **Widget 4: Llama 2**
    - Title: "Llama 2 Response"
    - Model: Llama
    - Prompt: Use the user input prompt by referencing the User Input widget with `@Enter Your Prompt`
    - Example: `@Enter Your Prompt`

### Configure Advanced Settings:
For each text generation widget, you can adjust the temperature and top P settings to explore different outputs.
- Example settings:
  - Temperature: 0.7
  - Top P: 0.9

### Add Static Text Widgets:
Use static text widgets to provide instructions and descriptions.
- Example:
  - "Instructions: Enter a prompt in the input field. The app will generate responses from four different AI models based on your prompt."
  - "Claude, Hiku, Titan, AI21Labs, and Cohere are the models used for generating the responses."

### Testing Your App:
1. Enter editing mode by clicking the "Edit" button at the upper-right corner of the app page.
2. Adjust the prompts and settings as necessary to fine-tune the output.
3. Test with various prompts to ensure the app behaves as expected.

### Making Your App Public:
1. Click on the "Make Public and Share" button to allow others to use your app.
2. Share the link with your friends or colleagues to gather feedback.

## Homework

### Exercise 3: Playtime with PartyRock

Can you update the prompts in your app, play with settings, or chain outputs together? Be creative and explore what PartyRock can do. Try adding a widget that can draw an image from the book.

### Remix an Application
With PartyRock, you can remix applications, which allows you to make a copy of an app in your account. From there, you can build and edit to make new changes. Remix your own apps to create new variations or remix public apps from friends or from sample apps. Try to remix one of the apps from the [PartyRock Discover page](https://partyrock.aws/discover).

### Create a Snapshot
Got a funny response from an app you’re using? You can share a snapshot with friends. Make sure the app is in public mode, then choose "Snapshot" in the top right corner of the app page. The URL that includes the current input and output of your app is then copied to your clipboard so you can share it with others.

## Exercise 4: Test with Different Prompt Complexity to Build the Same App

### FitCoach App Requirements 1

**App Requirements:** FitCoach app will help users achieve their fitness goals through personalized workout plans, basic nutrition tips, and progress tracking.

**Chatbot Assistant:** Pretend you are a fitness instructor. You suggested a basic workout plan and nutrition tips based on the user's personal information and goals. The user will now have a follow-up conversation with you.

### FitCoach App Requirements 2

**App Requirements:** FitCoach app will help users achieve their fitness goals through personalized workout plans, basic nutrition tips, and progress tracking.

**Inputs:**
- Age (Number input field)
- Weight (Number input field, units: kg or lbs)
- Height (Number input field, units: cm or ft/in)
- Goal Selection (Dropdown: Gain Muscle, Lose Weight, Maintain Fitness)

**Outputs:**
- Personalized workout plan (text)
- Nutrition tips (text)
- Sleep tips (text)

**Chatbot Assistant:** Pretend you are a fitness instructor. You suggested a basic workout plan and nutrition tips based on the user's personal information and goals. The user will now have a follow-up conversation with you.

### FitCoach App Requirements 3

**App Requirements:** FitCoach app will help users achieve their fitness goals through personalized workout plans, basic nutrition tips, and progress tracking.

**App Concept:** FitCoach is a comprehensive fitness companion application designed to provide personalized guidance, motivation, and a supportive community for individuals on their fitness journey.

**Purpose:** To create an engaging and user-friendly platform that promotes a fun, energetic atmosphere while empowering users to achieve their fitness goals through tailored workout plans, nutrition guidance, progress tracking, and social interaction.

**Target Audience:**
- **Primary Users:**
  - Individuals new to the gym or seeking structured guidance.
  - Users aiming to gain muscle, lose weight, or maintain their overall fitness.
  - Individuals seeking a supportive and motivating fitness community.
- **Secondary Users:**
  - Fitness enthusiasts looking for a comprehensive platform to manage their routines.
  - Coaches or trainers seeking a tool to remotely guide and monitor their clients.

**Core Features:**
- **Personalized Onboarding:**
  - Welcome Screen: Visually appealing and engaging welcome message (e.g., "Let's embark on your transformative fitness journey!") followed by a brief explanation of the purpose behind the information collection.
  - **Personal Information Input:**
    - Name (Text Number input field)
    - Gender (Dropdown menu: Male/Female)
    - Age (Number input field, validated for appropriate age range)
    - Weight (Number input field with units: kg)
    - Height (Number input field with units: cm)
    - Goal Selection (Input field with options: Gain Muscle, Lose Weight, Maintain Fitness with brief descriptions)
    - Workout Level (Input field: Beginner, Intermediate, Advanced)
    - Workout Frequency (Number input field with units: days per week)
    - Dietary Preferences (Options: Vegetarian, Vegan, Gluten-Free, Dairy-Free, etc.)
  - Data Utilization: Generate a personalized workout and nutrition plan tailored to the user's goals, fitness level, and preferences.
- **Goal-Oriented Training Plans:**
  - **Primary Goal Selection:** Allow users to select their primary fitness goal (e.g., Gain Muscle, Lose Weight, Maintain Fitness).
  - **Personalized Plans:** Create tailored workout plans considering user profiles, goals, and preferences.
  - **Plan Adaptability:** Plans should be adaptive and progressive, evolving with the user's fitness level and progress.
  - **Exercise Details:** Include detailed exercise instructions, recommended sets, reps, and rest periods.
  - **Plan Variety:** Offer a diverse range of workout plans (e.g., strength training, HIIT, yoga, cardio) to cater to different interests and goals.
  - **Plan Customization:** Allow users to customize their workout plans by swapping exercises or adjusting difficulty levels.
- **Nutrition Guidance:**
  - **Integration:** Sync with popular food tracking apps or incorporate a built-in food diary to monitor calorie and macro intake.
  - **Personalized Recommendations:** Offer daily calorie and macro recommendations based on the user's goals, activity levels, and dietary preferences.
  - **Meal Planning:** Provide healthy recipe suggestions, meal planning ideas, and grocery list creation tools.
  - **Educational Resources:** Offer educational content on nutrition, macronutrients, and healthy eating habits.
- **Motivational Community:**
  - **Social Feed:** Implement a platform for users to share their workouts, progress, motivational content, and connect with like-minded individuals.
  - **Gamification:** Introduce challenges, rewards, leaderboards, and virtual workout groups to foster engagement and friendly competition.
  - **Support System:** Enable users to connect with fitness buddies, coaches, or trainers for accountability and encouragement.
- **Progress Tracking:**
  - **Logging:** Allow users to log their workouts, weights lifted, body measurements, and progress photos.
  - **Visualization:** Display progress through charts, graphs, and before/after photo comparisons.
  - **Achievements:** Celebrate milestones and accomplishments with in-app rewards, badges, and celebrations.
  - **Integration:** Integrate with wearable fitness devices or activity trackers for seamless data synchronization.

**Widgets:**
- **Input Widgets:**
  - User's personal information (gender, age, weight, height, fitness level, goals, workout experience, workout frequency, dietary preferences)
  - User's goals and preferences
- **Output Widgets:**
  - Personalized workout plan (text)
  - Personalized nutrition plan (text)
  - Progress tracking charts (image/text)
  - Social feed updates (text)
  - Gamification elements (leaderboards, rewards) (text/image)
- **Chatbot Assistant:**
  - Pretend you are a fitness instructor. You suggested a workout plan and nutrition plan based on the user's personal information and goals. The user will now have a follow-up conversation with you.
