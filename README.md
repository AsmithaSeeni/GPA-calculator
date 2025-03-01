# GPA-calculator
def grade_to_points(grade):
    grade_map = {
        'O': 10,
        'A+': 9,
        'A': 8,
        'B+': 7,
        'B': 6,
        'C': 5,
        'U': 0,
        'RA': 0
    }
    return grade_map.get(grade.upper(), 0)
def calculate_gpa(grades, credits):
    total_points = 0
    total_credits = 0
    for grade, credit in zip(grades, credits):
        total_points += grade_to_points(grade) * credit
        total_credits += credit
    overall_gpa = total_points / total_credits
    return overall_gpa
data = {
    'CSE'or'cse'or'cs' or'computer science': {
        'Semester 1' or 'sem1'or 'sem 1' or'1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1 },
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Physics for Information Science(PH3256)':3,
                       'Basic Electrical and Electronics Engineering(BE3251)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Programming in C(CS3251)':3,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Programming in C Laboratory(CS3271)':2,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Discrete Mathematics(MA3354)':4,
                       'Digital Principles and Computer Organization(CS3351)':4,
                       'Foundations of Data Science(CS3352)':3,
                       'Data Structures(CS3301)':3,
                       'Object Oriented Programming(CS3391)':3,
                       'Data Structures Laboratory(CS3311)':1.5,
                       'Object Oriented Programming Laboratory(CS3381)':1.5,
                       'Data Science Laboratory(CS3361)':2,
                       'Professional Development(GE3361)':1},
        'Semester 4' :{'Theory of Computation(CS3452)':3,
                       'Artificial Intelligence and Machine Learning(CS3491)':4,
                       'Database Management Systems(CS3492)':3,'Algorithms(CS3401)':4,
                       'Introduction to Operating Systems(CS3451)':3,
                       'Environmental Sciences and Sustainability(GE3451)':2,
                       'Operating systems laboratory(CS3461)':1.5,
                       'Database Management Systems Laboratory(CS3481)':1.5},
        'Semester 5': {'Computer Networks(CS3591)':4,
                       'Compiler Design(CS3501)':4,
                       'Cryptography and Cyber Security(CB3491)':3,
                       'Distributed Computing(CS3551)':3,
                       'Professional Elective-1':3,
                       'Professional Elective-2':3},
        'Semester 6': {'Object Oriented Software Engineering(CCS356)':4,
                       'Embedded Systems and IoT(CS3691)':4,
                       'Open Elective-1':3,'Professional Elective-3':3,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3},
        'Semester 7' :{'Human Values and Ethics(GE3791)':2,
                       'Elective-Management':3,
                       'Open Elective-2':3,
                       'Open Elective-3':3,
                       'open Elective-4':3,
                       'Summer Internship(CS3711)':2},
        'Semester 8' :{'Project Work/Internship(CS3811)':10}
    },
    'AI&DS': {
        'Semester 1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1},
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Physics for Information Science(PH3256)':3,
                       'Basic Electrical and Electronics Engineering(BE3251)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Data structures Design(AD3251)':3,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Data Structures Design Laboratory(AD3271)':3,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Discrete Mathematics(MA3354)':4,
                       'Digital Principles and Computer Organization(CS3351)':4,
                       'Database Design and Management(AD3391)':3,
                       'Design and Analysis of Algorithms(AD3351)':4,
                       'Data Exploration and Visualization(AD3301)':4,
                       'Artificial Intelligence(AL3391)':3,
                       'Database Design and Management(AD3381)':1.5,
                       'Artificial Intelligence Laboratory(AD3311)':1.5,
                       'Professional Development-1(GE3361)':1},
        'Semester 4': {'Probability and Statistics(MA3391)':4,
                       'Operating Systems(AL3452)':4,
                       'Machine Learning(Al3451)':3,
                       'Fundamentals of Data Science and Analytics(AD3491)':3,
                       'Computer Networks(CS3591)':4,
                       'Environmental Sciences and Sustainability(GE3451)':2,
                       'Data Science and Analytics Laboratory(AD3411) ':2,
                       'Machine Learning Laboratory(AD3461)':2},
        'Semester 5': {' Deep Learning(AD3501)':3,
                       'Data and Information Security(CW3551)':3,
                       'Distributed Computing(CS3551)':3,
                       'Big Data Analytics(CCS334)':3,
                       'Professional Elective-1':3,
                       'Professional Elective-2':3,
                       'Deep Learning Laboratory(AD3511)':2,
                       'Summer internship(AD3512)':2},
        'Semester 6': {'Embedded Systems and IoT(CS3691)':4,
                       'Open Elective-1':3,
                       'Professional Elective-3':3,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3},
        'Semester 7': {'Human Values and Ethics(GE3791)':2,
                       'Elective-Management':3,
                       'Open Elective-2':3,
                       'Open Elective-3':3,
                       'Open Elective-4':3},
        'Semester 8': {'Project Work / Internship(AD3811)':10}
        },
    'Mech': {
        'Semester 1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1},
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Materials Science(PH3251)':3,
                       'Basic Electrical and Electronics Engineering(BE3251)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Basic Electrical and Electronics Engineering Laboratory(BE3271)':2,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Transforms and Partial Differential Equations(MA3351)':4,
                       'Engineering Mechanics(ME3351)':3,
                       'Engineering Thermodynamics(ME3391)':3,
                       'Fluid Mechanics and Machinery(CE3391)':4,
                       'Engineering Materials and Metallurgy(ME3392)':3,
                       'Manufacturing Processes(ME3393)':3,
                       'Computer Aided Machine Drawing(ME3381)':2,
                       'Manufacturing Technology Laboratory(ME3382)':2,
                       'Professional Development(GE3361)':1},
        'Semester 4': {'Theory of Machines(ME3491)':3,
                       'Thermal Engineering(ME3451)':4,
                       'Hydraulics and Pneumatics(ME3492)':3,
                       'Manufacturing Technology(ME3493)':3,
                       'Strength of Materials(CE3491)':3,
                       'Environmental Sciences and Sustainability(GE3451)':2,
                       'Strength of Materials and  Fluid Machinery Laboratory(CE3481)':2,
                       'Thermal Engineering Laboratory(ME3461)':2},
        'Semester 5': {'Design of Machine Elements(ME3591)':4,
                       'Metrology and Measurements(ME3592)':3,
                       'Professional Elective-1':3,
                       'Professional Elective-2':3,
                       'Professional Elective-3':3,
                       'Summer Internship(ME3511)':1,
                       'Metrology and Dynamics Laboratory(ME3581)':2},
        'Semester 6': {'Heat and Mass Transfer(ME3691)':4,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3,
                       'Professional Elective-7':3,
                       'CAD/CAM Laboratory(ME3681)':2,
                       'Heat Transfer Laboratory(ME3682)':2},
        'Semester 7': {'Mechatronics and IoT(ME3791)':3,
                       'Computer Integrated Manufacturing(ME3792)':3,
                       'Human Values and Ethics(GE3791)':2,
                       'Industrial Management(GE3792)':3,
                       'Open Elective-2':3,
                       'Open Elective-3':3,
                       'Open Elective-4':3,
                       'Mechatronics and IoT Laboratory(ME3781)':2,
                       'Summer Internship(ME3711)':1},
        'Semester 8': {'Project Work / Internship(ME3811)':10}
        },
    'ECE': {
        'Semester 1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1},
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Physics for Electronics Engineering(PH3254)':3,
                       'Electronics and Instrumentation Engineering(BE3254)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Circuit Analysis(EC3251)':4,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Circuit Analysis Laboratory(EC3271)':1,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Random Processes and Linear Algebra(MA3355)':4,
                       'C Programming and Data Structures(CS3353)':3,
                       'Signals and Systems(EC3354)':4,
                       'Electronic Devices and Circuits(EC3353)':3,
                       'Control Systems(EC3351)':3,
                       'Digital Systems Design(EC3352)':4,
                       'Electronic Devices and Circuits Laboratory(EC3361)':1.5,
                       'C Programming and Data Structures Laboratory(CS3362)':1.5,
                       'Professional Development(GE3361)':1},
        'Semester 4': {'Electromagnetic Fields(EC3452)':3,
                       'Networks  and Security(EC3401)':4,
                       'Linear Integrated Circuits(EC3451)':3,
                       'Digital Signal Processing(EC3492)':4,
                       'Communication Systems(EC3491)':3,
                       'Environmental Sciences and Sustainability(GE3451)':2,
                       'Communication Systems Laboratory(EC3461)':1.5,
                       'Linear Integrated Circuits Laboratory(EC3462)':1.5},
        'Semester 5': {'Wireless Communication(EC3501)':4,
                       'VLSI and Chip Design(EC3552)':3,
                       'Transmission lines and RF Systems(EC3551)':3,
                       'Professional Elective-1':3,
                       'Professional Elective-2':3,
                       'Professional Elective-3':3,
                       'VLSI Laboratory(EC3561)':2},
        'Semester 6': {'Embedded Systems and IOT Design(ET3491)':4,
                       'Artificial Intelligence and Machine Learning(CS3491)':4,
                       'Open Elective-1':3,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3},
        'Semester 7': {'Human Values and Ethics(GE3791)':2,
                       'Elective - Management':3,
                       'Open Elective-2':3,
                       'Open Elective-3':3,
                       'Open Elective-4':3,
                       'Summer internship(EC3711)':2},
        'Semester 8': {'Project Work / Internship(EC3811)':10}
        },
    'EEE': {
        'Semester 1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1},
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Physics for Electrical Engineering(PH3202)':3,
                       'Basic Civil and Mechanical Engineering(BE3255)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Electric Circuit Analysis(EE3251)':4,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Electric Circuits Laboratory(EE3271)':2,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Probability and Complex Functions(MA3303)':4,
                       'Electromagnetic Fields(EE3301)':4,
                       'Digital Logic Circuits(EE3302)':3,
                       'Electron Devices and Circuits(EC3301)':3,
                       'Electrical  Machines - I(EE3303)':3,
                       'C Programming and Data Structures(CS3353)':3,
                       'Electronic Devices and Circuits Laboratory(EC3311)':1.5,
                       'Electrical  Machines Laboratory-1(EE3311)':1.5,
                       'C Programming and Data Structures Laboratory(CS3362)':1.5,
                       'Professional Development(GE3361)':1},
        'Semester 4': {'Environmental Sciences and Sustainability(GE3451)':2,
                       'Transmission and Distribution(EE3401)':3,
                       'Linear Integrated Circuits(EE3402)':3,
                       'Measurements and Instrumentation(EE3403)':3,
                       'Microprocessor and Microcontroller(EE3404)':3,
                       'Electrical Machines - II(EE3405)':3,
                       'Electrical Machines Laboratory - II(EE3411)':1.5,
                       'Linear and Digital Circuits Laboratory(EE3412)':1.5,
                       'Microprocessor and Microcontroller laboratory(EE3413)':1.5},
        'Semester 5': {'Power System Analysis(EE3501)':3,
                       'Power Electronics(EE3591)':3,
                       'Control Systems(EE3503)':3,
                       'Professional Elective-1':3,
                       'Professional Elective-2':3,
                       'Professional Elective-3':3,
                       'Power Electronics Laboratory(EE3511)':1.5,
                       'Control and Instrumentation Laboratory(EE3512)':2},
        'Semester 6': {'Protection and Switchgear(EE3601)':3,
                       'Power System Operation and Control(EE3602)':3,
                       'Open Elective-1':3,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3,
                       'Power System Laboratory(EE3611)':1.5},
        'Semester 7': {'High Voltage Engineering(EE3701)':3,
                       'Human Values and Ethics(GE3791)':2,
                       'Elective – Management':3,
                       'Open Elective-2':3,
                       'Open Elective-3':3,
                       'Open Elective-4':3,
                       'Professional Elective-7':3},
        'Semester 8': {'Project Work / Internship(EE3811)':10}
        },
    'Civil': {
        'Semester 1': {'Professional English-1(HS3152)':3,
                       'Matrices and Calculas(MA3151)':4,
                       'Engineering Physics(PH3151)':3,
                       'Engineering Chemistry(CY3151)':3,
                       'Problem Solving and Python Programming(GE3151)':3,
                       'Heritage of Tamils(GE3152)':1,
                       'Problem Solving and Python Programming Laboratory(GE3171)':2,
                       'Physics and Chemistry Laboratoty(BS3171)':2,
                       'English Laboratory(GE3172)':1},
        'Semester 2': {'Professional English-2(HS3252)':2,
                       'Statistics and Numerical Methods':4,
                       'Physics for Civil Engineering(PH3201)':3,
                       'Basic Electrical, Electronics and Instrumentation Engineering(BE3252)':3,
                       'Engineering Graphics(GE3251)':4,
                       'Electric Circuit Analysis(EE3251)':4,
                       'Tamils and Technology(GE3252)':1,
                       'Engineering Practices Laboratory(GE3271)':2,
                       'Basic Electrical,Electronics and Instrumentation Engineering Laboratory(BE3272)':2,
                       'Communication Laboratory/Foreign Language(GE3272)':2},
        'Semester 3': {'Transforms and Partial Differential Equations(MA3351)':4,
                       'Engineering Mechanics(ME3351)':3,'Fluid Mechanics(CE3301)':3,
                       'Construction Materials and Technology(CE3302)':3,
                       'Water Supply and Wastewater Engineering(CE3303)':4,
                       'Surveying and Levelling(CE3351)':3,
                       'Surveying and Levelling Laboratory(CE3361)':1.5,
                       'Water and Wastewater Analysis Laboratory(CE3311)':1.5,
                       'Professional Development(GE3361)':1},
        'Semester 4': {'Applied Hydraulics Engineering(CE3401)':4,
                       'Strength of Materials(CE3402)':3,
                       'Concrete Technology(CE3403)':3,
                       'Soil Mechanics(CE3404)':3,
                       'Highway and Railway  Engineering(CE3405)':3,
                       'Environmental Sciences and Sustainability(GE3451)':2,
                       'Hydraulic Engineering Laboratory(CE3411)':1.5,
                       'Materials Testing Laboratory(CE3412)':2,
                       'Soil Mechanics Laboratory(CE3413)':1.5},
        'Semester 5': {'Design of Reinforced Concrete Structural Elements(CE3501)':3,
                       'Structural Analysis I(CE3502)':3,
                       'Foundation Engineering(CE3503)':3,
                       'Professional Elective-2':3,
                       'Professional Elective-3':3,
                       'Professional Elective-4':3,
                       'Highway Engineering Laboratory(CE3511)':2,
                       'Survey Camp(CE3512)':1},
        'Semester 6': {'Design of Steel Structural Elements(CE3601)':3,
                       'Structural Analysis II(CE3602)':3,
                       'Professional Elective-4':3,
                       'Professional Elective-5':3,
                       'Professional Elective-6':3,
                       'Open Elective – I':3,
                       'Building Drawing and Detailing Laboratory(CE3611)':2},
        'Semester 7': {'Estimation, Costing and Valuation Engineering(CE3701)':3,
                       'Hydrology and Water Resources Engineering(AI3404)':3,
                       'Human Values and Ethics(GE3791)':2,
                       'Total Quality Management(GE3752)':3,
                       'Open Elective-2':3,'Open Elective-3':3,
                       'Open Elective-4':3},
        'Semester 8': {'Project Work/Internship(CE3811)':10}
        }
    }
def main():
    department = input("Enter your department: ")
    if department not in data:
        print("Department not found!")
        return
    semester = input(f"Enter your semester : ")
    if semester not in data[department]:
        print("Semester not found!")
        return
    subjects_credits = data[department][semester]
    grades = []
    credits = []
    for subject, credit in subjects_credits.items():
        grade = input(f"Enter your grade for {subject} : ")
        grades.append(grade)
        credits.append(credit)
    gpa = calculate_gpa(grades, credits)
    print(f"Your GPA for {semester} in {department} is: {gpa:.2f}")
if __name__ == "__main__":
    main()
