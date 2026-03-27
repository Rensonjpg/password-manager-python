# password-manager-python
Secure Password Manager using Python




# 📊 Data Analyzer

students = {
    "Rahul": 85,
    "Riya": 92,
    "Aman": 76,
    "Neha": 88,
    "Raman": 33
}

def show_data():
    print("\n📋 Student Data:\n")
    for name, marks in students.items():
        print(f"{name} → {marks}")

def average_marks():
    avg = sum(students.values()) / len(students)
    print("\n📈 Average Marks:", round(avg, 2))

def topper_lowest():
    topper = max(students, key=students.get)
    lowest = min(students, key=students.get)
    print(f"\n🏆 Topper: {topper} → {students[topper]}")
    print(f"📉 Lowest: {lowest} → {students[lowest]}")

def pass_fail():
    # assume pass mark = 40
    pass_count = sum(1 for m in students.values() if m >= 40)
    fail_count = sum(1 for m in students.values() if m < 40)
    print(f"\n✅ Pass Students: {pass_count}")
    print(f"❌ Fail Students: {fail_count}")

def search_student():
    name = input("\nEnter student name: ")
    if name in students:
        print("\n🔍 Found:")
        print(f"{name} → {students[name]}")
    else:
        print("\n❌ Student not found")

def main():
    while True:
        print("\n📊 Data Analyzer")
        print("1. Show Data")
        print("2. Average Marks")
        print("3. Topper / Lowest")
        print("4. Pass / Fail Count")
        print("5. Search Student")
        print("6. Exit")
        
        choice = input("Enter choice: ")
        if choice == "1":
            show_data()
        elif choice == "2":
            average_marks()
        elif choice == "3":
            topper_lowest()
        elif choice == "4":
            pass_fail()
        elif choice == "5":
            search_student()
        elif choice == "6":
            print("\nThank You 👋")
            break
        else:
            print("Invalid choice")

if __name__ == "__main__":
    main()
