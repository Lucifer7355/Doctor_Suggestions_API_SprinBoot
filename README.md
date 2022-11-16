# Doctor_Suggestions_API_SprinBoot

### The Task
We have a platform where doctors can register their patients through a mobile or web portal. For this to work we need to build backend APIs to achieve task like:
Adding a doctor
Adding a patient & it’s symptom
Suggesting the doctor based on patient’s symptom

### Doctor’s entity
In our database we will have doctor’s name, city, email, phone number and speciality.
City can have 3 values only i.e. Delhi, Noida, Faridabad
Speciality can have 4 values i.e. Orthopedic, Gynecology, Dermatology, ENT specialist
A doctor can be added or removed from the platform.

### Patient’s entity
In our database we will have patient’s name, city, email, phone number and symptom.
City can have any value
Symptom can have the following values only
Arthritis, Backpain, Tissue injuries (comes under Orthopedic speciality)
Dysmenorrhea (comes under Gynecology speciality)
Skin infection, skin burn (comes under Dermatology speciality)
Ear pain (comes under ENT speciality)
A patient can be added or removed from the platform.

Following fields should have the mentioned validations at the backend:
Name (should be at least 3 characters)
City (should be at max 20 characters)
Email (should be a valid email address)
Phone number (should be at least 10 number)

### Suggesting Doctors
This API will accept patient ID, and on calling this API, it will suggest the doctors based out of the patient location and the patient symptom.

Important Note: This is the evaluating API where the logic needs to be working. The suggested doctor in the API should be based on the symptom of the patient that links to doctor’s speciality. E.g.  If a patient have Eye pain then only ENT specialist doctor should be suggested.
Edge-Case 1: If there isn’t any doctor on that location (i.e. outside Delhi, Noida, Faridabad), the response should be “We are still waiting to expand to your location”
Edge-Case 2: If there isn’t any doctor for that symptom on that location, the response should be “There isn’t any doctor present at your location for your symptom”
