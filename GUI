import tkinter as tk

def calculate_egfr():
    # Get user inputs from the GUI fields
    age = float(age_entry.get())
    gender = gender_entry.get()
    serum_creatinine = float(creatinine_entry.get())
    race = float(race_entry.get())

    try:
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

        # Update the result label in the GUI
        result_label.config(text="Estimated GFR: {} mL/min/1.73m²".format(egfr))

    except ValueError as e:
        # Display error message in the GUI
        result_label.config(text="Error: {}".format(str(e)))

# Create the main window
window = tk.Tk()
window.title("eGFR Calculator")

# Create labels and entry fields for user inputs
age_label = tk.Label(window, text="Age (in years):")
age_label.pack()
age_entry = tk.Entry(window)
age_entry.pack()

gender_label = tk.Label(window, text="Gender (male/female):")
gender_label.pack()
gender_entry = tk.Entry(window)
gender_entry.pack()

creatinine_label = tk.Label(window, text="Serum Creatinine (in mg/dL):")
creatinine_label.pack()
creatinine_entry = tk.Entry(window)
creatinine_entry.pack()

race_label = tk.Label(window, text="Race Adjustment Factor:")
race_label.pack()
race_entry = tk.Entry(window)
race_entry.pack()

# Create a button to calculate eGFR
calculate_button = tk.Button(window, text="Calculate", command=calculate_egfr)
calculate_button.pack()

# Create a label to display the result
result_label = tk.Label(window, text="")
result_label.pack()

# Start the GUI event loop
window.mainloop()
