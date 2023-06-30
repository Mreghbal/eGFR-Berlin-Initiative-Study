def calculate_egfr(age, gender, serum_creatinine, race):
    # Validate input values
    if age <= 0 or serum_creatinine <= 0:
        raise ValueError("Age and serum creatinine must be greater than 0.")
    
    # Check gender and assign respective constants and multipliers
    if gender.lower() == 'male':
        k = 0.9
        a = -0.411
    elif gender.lower() == 'female':
        k = 0.7
        a = -0.329
    else:
        raise ValueError("Invalid gender. Please specify 'male' or 'female'.")
    
    # Calculate eGFR
    egfr = k * (min(serum_creatinine / a, 1) ** a) * ((max(serum_creatinine / a, 1) ** (-1.209)) * (age ** (-0.20))) * race
    
    return egfr

try:
    # Get user inputs
    age = float(input("Enter age (in years): "))
    gender = input("Enter gender (male/female): ")
    serum_creatinine = float(input("Enter serum creatinine (in mg/dL): "))
    race = float(input("Enter race adjustment factor (1 for non-black, 1.159 for black): "))
    
    # Call the function to calculate eGFR
    eGFR = calculate_egfr(age, gender, serum_creatinine, race)
    
    # Print the result
    print("Estimated GFR:", eGFR, "mL/min/1.73m²")
    
except ValueError as e:
    print("Error:", str(e))
