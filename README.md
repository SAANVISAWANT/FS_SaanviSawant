# FS_SaanviSawant
A student-focused carpooling app that matches nearby routes, keeps identities anonymous, and sparks chats based on common interests. Unlike generic ride-sharing apps, it’s built to make commuting safer, smarter, and more social for students.
# 🚗 Student Commute Optimizer  

## 🌟 Why I Created This Project  
As a student, I noticed many of us travel alone every day. This not only increases costs and traffic but also raises safety concerns. I wanted to design a solution that helps students **find safe commute partners**, save money, and make commuting more social.  

## 🎯 My Goal  
- Build a platform designed **exclusively for students**  
- Encourage **carpooling & route-sharing** in a secure way  
- Make commuting **cheaper, safer, and more interactive**  
- Create a **community feel** by letting students connect beyond just rides  

## 🔑 Uniqueness  
Unlike generic ride-sharing apps, this project is:  
- 🛡️ **Anonymous & Safe** → students connect using unique usernames, not personal details  
- 🗺️ **Route & Direction Aware** → matches aren’t random, they’re based on shared travel paths  
- 💬 **Interest-Based Chat** → suggests topics so rides aren’t awkward, but engaging  
- 🎓 **Student-Centric** → built only for campus life, with focus on trust and community  
## 🖥️ Step 1: Frontend Idea & Uniqueness  

### 💡 My Idea (Frontend)  
The frontend is the **student-facing part** of the application. It will provide:  
- A **map-based interface** where students enter their starting point and destination.  
- A **dashboard** that shows nearby students traveling in the same direction.  
- An option to **click on student icons** on the map to either:  
  - Start an **anonymous chat**  
  - View **common interests** to spark conversations  

### 🔧 Technical Choices (Frontend Stack)  
Frontend: React/Next.js with Google Maps API to show routes & nearby students.
Authentication: Students log in with Profile IDs (no real names).
Matching Engine: Compares route tokens to find students traveling in the same direction.
Interests Engine: Suggests common interests when two students connect.
Chat System: Real-time chat via WebSockets/Firebase, anonymous with profile IDs.
Database: MongoDB/Firebase stores only hashed IDs, routes, and interests (no personal info).
Privacy: JWT-based login, anonymized data, temporary chat storage for safety. 

## 🧩 Pseudocode (Frontend Flow)

```pseudo
function main():
    showLandingPage()
    if userSelects("Register"):
        registerUser()
    else if userSelects("Login"):
        loginUser()

function registerUser():
    collect(name, email, password, interests)
    saveToDatabase(name, email, hash(password), interests)
    redirectToDashboard()

function dashboard():
    home, destination = getUserInput()
    displayMap(home, destination)
    nearbyStudents = findNearbyStudents(home, destination)
    for student in nearbyStudents:
        showIcon(student)
        if userClicks(studentIcon):
            openChat(student)
        if userClicks("View Interests"):
            showCommonInterests(student)
```


### 🔑 Uniqueness in Frontend  
- 🛡️ **Anonymous Communication** → Students are identified only by a **Profile ID** (not real names), protecting privacy.  
- 💬 **Interest-Based Suggestions** → When a student opens the chat, the system highlights **shared interests** (e.g., music, sports, books) to make conversations natural and friendly.  
- 🎓 **Student-Centric Flow** → Unlike general ride-sharing apps, the frontend is designed specifically for **student communities**, focusing on safety and meaningful interaction.  
<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/b5ddf1b9-99ff-47b1-80fc-25470f2e6197" />




**🎯 Backend Aim**

The backend is designed to ensure smart, safe, and social commuting for students by:

- 🔍 Comparing student routes in real-time to detect overlapping paths.  
- 📍 Considering proximity and travel direction, not just raw distance.  
- 🤝 Suggesting carpool matches ranked by the quality of route overlap and shared interests.  
- 🛡️ Guaranteeing user anonymity through unique, non-duplicable Profile IDs.  
- ✨ Enhancing conversations by attaching common interests to match suggestions.  
- ⏳ Enforcing privacy with temporary, ephemeral chat channels that prevent long-term data storage.


**Technical Specification**

- **Smart Matching:** Matches factor in time, direction, and distance — not just the nearest location.  
- **Unique IDs:** Profile IDs are generated using a hashing mechanism with duplication checks to ensure uniqueness.  
- **Interest Layer:** Every match suggestion includes shared interests to keep conversations engaging from the start.  
- **Anonymous Chat Rooms:** Students communicate exclusively through temporary chat channels with no personal data revealed.  
- **Privacy-by-Design:** Only minimal, anonymized data is stored — such as route tokens, hashed IDs, and interests.

**Enhancements & Next Features**

- Improve the route matching algorithm for greater accuracy and efficiency.  
- Add customizable user profiles and personal settings.  
- Implement notifications for new matches and incoming chat messages.  
- Enable scheduling of rides and support for recurring routes.  
- Develop an analytics dashboard for administrators to monitor usage and performance.  

**CONCLUSION**

- The Student Commute Optimizer is a community-driven platform designed exclusively for students.  
- It prioritizes anonymity, ensuring users connect safely without sharing personal details.  
- Matches are smart and route-based, considering direction, overlap, and shared interests.  
- The platform transforms commuting into a social, cost-effective, and safer experience.  
- It empowers students to build connections and fosters a stronger campus community.  
- Join us in making student commuting **cheaper, safer, and more connected—one ride at a time!**
