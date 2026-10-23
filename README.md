def calculate_grade(average):
    if average >= 90:
        return "A"
    elif average >= 80:
        return "B"
    elif average >= 70:
        return "C"
    elif average >= 60:
        return "D"
    else:
        return "F"

def analyze_marks():
    subjects = ["Math", "Science", "English"]

    marks = []
    for subject in subjects:
        mark = float(input(f"Enter marks for {subject}: "))
        marks.append(mark)

    total = sum(marks)
    average = total / len(marks)
    grade = calculate_grade(average)

    print("\nStudent Mark Analysis")
    print("-" * 30)
    for i, subject in enumerate(subjects):
        print(f"{subject}: {marks[i]}")
    print(f"Total Marks: {total}")
    print(f"Average Marks: {average:.2f}")
    print(f"Grade: {grade}")

# Run the program
analyze_marks()
