# 🚗 RouteSmart: AI-Driven Road Navigation Application
**RouteSmart** is an AI-driven road navigation application designed by team **LogiCode**, RouteSmart aims to provide users with intelligent, voice-activated navigation assistance, addressing the challenges of urban traffic congestion and the limitations of traditional navigation systems. This project leverages AI concepts to offer real-time, adaptive routing, personalized suggestions, and enhanced safety features, primarily through a conversational interface (chatbot) and a supporting UI design.
<br><br>

### 🚦 Problem Statement
Traffic congestion is a major issue in modern cities, impacting commuters and emergency services alike. Key problems addressed include:
*   **Inefficiency of Traditional Systems:** Static navigation apps and fixed traffic signals often fail to adapt to dynamic, real-time traffic conditions (congestion, accidents, road closures).
*   **Commuter Frustration:** Leads to delays, lost productivity, wasted fuel, and increased stress.
*   **Impeded Emergency Response:** Congestion delays critical, life-saving interventions by emergency responders (ambulance, fire, police).
*   **Lack of Personalization:** Standard navigation apps often don't cater to specific user needs (e.g., finding amenities, avoiding specific zones, hands-free operation).
*   **Safety Concerns:** Manual interaction with navigation apps while driving poses safety risks.
<br>

### 🎯 Objectives
RouteSmart aims to create an intelligent navigation agent that:
1.  Provides **efficient navigation** by finding optimal routes based on real-time data.
2.  **Minimizes delays** by dynamically adjusting routes to avoid congestion and incidents.
3.  Enhances user **safety** through hands-free, voice-activated controls.
4.  Supports **emergency response** by prioritizing routes for emergency vehicles and alerting nearby users.
5.  Offers a **personalized** and **convenient** user experience.
<br>

### 💡 Proposed Solution: RouteSmart
RouteSmart is designed as an AI agent that acts as an intelligent navigation assistant. It integrates real-time data processing, user interaction (primarily voice), and adaptive routing based on user preferences and current conditions.
#### Key Features:
*   **AI-Powered Real-Time Routing:** Analyzes real-time traffic data, incidents, and weather to suggest the most efficient routes.
*   **Voice-Activated Commands:** Enables hands-free operation for setting destinations, requesting route changes, or adding stops (e.g., petrol stations), enhancing safety.
*   **Dynamic Route Adjustment:** Automatically suggests or adjusts routes based on detected congestion or incidents.
*   **Personalization:** Allows users to request nearby amenities (POIs) and adapts suggestions based on learned preferences (conceptual).
*   **Emergency Route Prioritization:** Identifies and prioritizes routes for emergency responders, notifying other users to clear the path (conceptual).
*   **Contextual Understanding:** Interprets complex user commands like "avoid accidents" or "find the nearest petrol station".
*   **Conversational Interface:** Uses a chatbot (Botpress) for natural language interaction.
*   **UI Visualization:** Provides a visual representation of the route, map, and directions (Figma).
<br>

### 🧠 AI Concepts & Methodology
RouteSmart's intelligence is built upon fundamental AI principles:
#### Intelligent Agent (PEAS Model)
The core of RouteSmart is modeled as a rational agent:
*   **Performance Measure:** Efficient navigation, Minimize delays, Safety, Emergency response effectiveness.
*   **Environment:** Roads, Other vehicles, Traffic conditions, Amenities (POIs), Weather, User inputs.
*   **Actuators:** Route adjustments, Alerts (traffic, safety, emergency), Emergency route prioritization, User feedback prompts.
*   **Sensors:** GPS, Traffic detectors (real-time data APIs), User input (voice, text), potentially vehicle sensors (conceptual).

*(See [Assignment 3](https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment3.pdf) for detailed PEAS breakdown)*


#### State Space Search
The navigation process is modeled as a search problem:
*   **States:** Represent conditions like Internet connectivity, Navigation status, Traffic detection, Hands-free mode status, Information extraction, Amenity inclusion, Emergency request status, Route updating status.
*   **Initial State:** Checking Internet connectivity.
*   **Actions:** Transitions between states triggered by real-time data or user input (e.g., Detect Traffic -> Alert, Request Amenity -> Adjust Route).
*   **Goal State:** Route Updated (optimal path finalized based on current info).
*   **Path Cost:** Represents computational expense, time delays, fuel consumption, etc., associated with actions.

*(See [Assignment 2](https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment2.pdf) for State Space Diagram and Formulation)*


#### Knowledge Representation (FOL)
Logical rules define the agent's decision-making:
*   Rules are defined using First-Order Logic (FOL) to handle conditions like:
    *   Adjusting routes for congestion (`IF traffic_congestion = TRUE AND auto_adjust = ON THEN ...`).
    *   Handling different input modes (voice vs. typing, hands-free on/off).
    *   Calculating recommended departure times based on arrival goals and traffic.
    *   Including nearby amenities upon request.
    *   Responding to detected traffic incidents with alerts and alternative routes.
    *   Prioritizing emergency route requests.

*(See [Assignment 1](https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment1.pdf) for detailed FOL rules)*


#### Agent Behavior
The AI agent gathers real-time data, processes it using inference rules (based on the Knowledge Representation), considers user preferences and context, and provides optimized, adaptive navigation suggestions via the actuators (chatbot responses, route changes). It aims for efficiency, safety, and user convenience.
<br><br>

### 🛠️ Technology & Implementation
#### Working Prototypes
This project delivers functional prototypes for key components:
*   **Conversational Agent:** Implemented using **Botpress Cloud**, handling user interaction, information gathering, API calls (simulated/actual for Google Maps), and providing navigation instructions.
*   **User Interface (UI):** Designed using **Figma**, visualizing the user flow from landing page to navigation, route adjustments, and completion.
<br>

### ✨ Working Prototypes
Explore the implemented components of RouteSmart:
#### Botpress Chatbot
Interact with the conversational AI agent designed to handle navigation requests:
*   [Launch Chatbot](https://cdn.botpress.cloud/webchat/v2.2/shareable.html?configUrl=https://files.bpcontent.cloud/2025/01/15/11/20250115110759-Q476XGLP.json)
> **How to Use:**
> 1. Click the link above to open the Botpress web chat.
> 2. Follow the prompts to provide origin, destination, and other requests (e.g., "add stop", "faster route").
> 3. The chatbot uses Google Maps APIs to calculate routes, times, and generate map images.

#### Figma UI Prototype
Visualize the intended user interface and flow of the mobile application:
*   [Explore UI Prototype](https://www.figma.com/proto/CSLqQ8015h037qplHEPL5a/RouteSmart?node-id=1-201&p=f&t=HkjnAuviaq0JYxzU-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A201&show-proto-sidebar=1&hide-ui=1)
> **How to Use:**
> 1. Click the link above to open the Figma prototype.
> 2. Navigate through the screens simulating the user journey from starting the app to completing navigation.
> 3. Refer to the [Project Documentation (Section 2.0)](https://github.com/kohxuan/RouteSmart/blob/main/docs/ProjectDocumentation.pdf) for explanations of the UI flow and screen components.
<br>

### 📚 Project Documentation
Detailed information about the project's concept, design, AI implementation, and prototypes can be found in the following documents:
| Document             | Link                                                                                                                               | Focus                             |
| :------------------- | :--------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------- |
| Project Proposal     | <a href="https://github.com/kohxuan/RouteSmart/blob/main/docs/Proposal.pdf" ><img src="https://github.com/user-attachments/assets/680fbc90-1078-4a35-8178-841f158b8f16" width="24px" height="24px" ></a>                    | Initial Concept, Problem, Vision        |
| Assignment 1         | <a href="https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment1.pdf" ><img src="https://github.com/user-attachments/assets/680fbc90-1078-4a35-8178-841f158b8f16" width="24px" height="24px" ></a>                    | Knowledge Representation (FOL)          |
| Assignment 2         | <a href="https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment2.pdf" ><img src="https://github.com/user-attachments/assets/680fbc90-1078-4a35-8178-841f158b8f16" width="24px" height="24px" ></a>                    | State Space Search                      |
| Assignment 3         | <a href="https://github.com/kohxuan/RouteSmart/blob/main/docs/Assignment3.pdf" ><img src="https://github.com/user-attachments/assets/680fbc90-1078-4a35-8178-841f158b8f16" width="24px" height="24px" ></a>                    | Intelligent Agent (PEAS)                |
| Final Project Doc    | <a href="https://github.com/kohxuan/RouteSmart/blob/main/docs/ProjectDocumentation.pdf" ><img src="https://github.com/user-attachments/assets/680fbc90-1078-4a35-8178-841f158b8f16" width="24px" height="24px" ></a>       | Botpress & Figma Prototypes Explanation |
<br>

### 🤝 Team: LogiCode
| Name                                                  | Matric No. |
| :-------------------                                  | :--------- |
| [Maisarah Binti Rizal](https://github.com/mysarahzal) | A22EC0192  |
| [Koh Li Hui](https://github.com/kohlihui)             | A22EC0059  |
| [Koh Su Xuan](https://github.com/kohxuan)             | A22EC0060  |
| [Tang Yan Qing](https://github.com/yan-qing09)        | A22EC0109  |
<br>
