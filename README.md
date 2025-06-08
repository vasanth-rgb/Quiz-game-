def run_quiz(questions):
    score = 0
    for question in questions:
        print("\n" + question["question"])
        for option in question["options"]:
            print(option)
        answer = input("Enter your answer (A/B/C/D): ").strip().upper()
        if answer == question["answer"]:
            print("✅ Correct!")
            score += 1
        else:
            print(f"❌ Wrong! The correct answer was {question['answer']}")
    print(f"\nYour final score is: {score}/{len(questions)}")


quiz_questions = [
    {
        "question": "What is the capital of France?",
        "options": ["A. Paris", "B. London", "C. Rome", "D. Madrid"],
        "answer": "A"
    },
    {
        "question": "Which planet is known as the Red Planet?",
        "options": ["A. Earth", "B. Mars", "C. Jupiter", "D. Saturn"],
        "answer": "B"
    },
    {
        "question": "Who wrote 'Macbeth'?",
        "options": ["A. Charles Dickens", "B. William Shakespeare", "C. Jane Austen", "D. Mark Twain"],
        "answer": "B"
    },
    {
        "question": "What is the largest ocean on Earth?",
        "options": ["A. Atlantic Ocean", "B. Indian Ocean", "C. Pacific Ocean", "D. Arctic Ocean"],
        "answer": "C"
    }
]

if __name__ == "__main__":
    print("🧠 Welcome to the Quiz Game!")
    run_quiz(quiz_questions)
