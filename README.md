# 🤖 GPT-4V Solver for Enem 2023 📚

This project leverages the [GPT-4V model](https://cdn.openai.com/papers/GPTV_System_Card.pdf) from OpenAI to tackle questions from Brazil's Enem 2023 exam.

As an initial experiment, I asked the model to solve the mathematics questions. It got 35% accuracy.

## 🛠 Setup Instructions

Follow these steps to get the Enem solver up and running:

1. Clone the repo with the Enem 2023 exam content.
2. Inside the `ENEM23` directory, whip up a `.env` file with your OpenAI API key (note: this API key needs to have access to GPT-4V):
3. 🗝️ Create a `.env` file within the project directory and insert your OpenAI API key like so:

    ```env
    OPENAI_API_KEY=your_api_key_here
    ```

4. 📸 Screenshot the questions from the exam's PDF and save them into the `questions` folder. Name each screenshot file with its question number followed by the '.png' extension. For example, name the files as 1.png, 2.png, 3.png, and so on. This naming convention is essential for the script to identify and process each question correctly. Note: currently, we have all 45 math questions screenshots in the folder.

5. 🚀 Execute the `run_enem_2023_solver.ipynb` notebook to begin the question-solving process.

## 📌 Dependencies

Ensure you have the necessary libraries by running:

    pip install requests python-dotenv

## 🎯 Execution Results

- **Total Questions Processed**: The total number of images in the `questions` folder.
- **Retries**: The number of times the API call was retried.
- **Accuracy**: The model achieved correct answer rate.
- **Time Taken**: The duration from start to finish of the question-solving process.

## 📂 Repository Structure

- `questions/`: Contains the images of the exam questions.
- `reasoning/`: Stores the text files where the model's reasoning is explained.
- `Enem 2023 - Enem 2023 - Caderno de questões da prova amarela do 2º dia`: The exam's PDF.
- `marking_scheme.txt`: The text file with the correct answers (currently holding a non-oficial marking_scheme from O Globo and Etapa).
- `run_enem_2023_solver.ipynb`: The Jupyter notebook to execute the solver.