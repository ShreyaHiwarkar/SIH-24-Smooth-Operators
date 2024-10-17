# SIH-2024-Smooth-Operators



---

### **Problem Statement:**  
**Development of map-matching algorithm using AI-ML techniques to distinguish vehicular movement on highway and service road**

---

### **Description**  
This project focuses on developing a robust map-matching algorithm using artificial intelligence (AI) and machine learning (ML) techniques to distinguish vehicular movement on highways and service roads. The solution aims to function even when GNSS data is intermittent or contains large biases. The algorithm is intended to support GNSS-based tolling applications, helping to enhance the efficiency of toll collection and traffic management.

Key objectives:
1. Distinguish vehicle movement on highways vs service roads using coarse GNSS data.
2. Utilize AI-ML techniques to improve map-matching performance, even with suboptimal GNSS signals.
3. Apply the algorithm to tolling systems to streamline operations and reduce errors.

---

### **Prerequisites**
1. **Python** (for AI-ML algorithm development)
2. **Machine Learning Libraries**: scikit-learn, TensorFlow/PyTorch
3. **Geospatial Libraries**: Geopandas, Shapely, or GDAL
4. **Map-Matching Algorithms**: Understanding of map-matching concepts and algorithms
5. **GNSS Data Handling**: Knowledge of GPS/GNSS systems and data processing
6. **Data Visualization**: Matplotlib, Plotly for visualizing vehicle paths
7. **AI-ML Algorithms**: Experience with classification, regression, or clustering models
8. **Basic AI/ML Concepts**: Supervised/unsupervised learning, model training, validation, and testing

---

### **Proposed Solution**
To solve the challenge of distinguishing whether a vehicle is on the highway or service road using intermittent or biased GNSS data, we’ve developed a systematic approach that combines map-matching algorithms and AI-ML techniques to deliver accurate results.

**Step 1: Data Collection and Preprocessing**
We start by collecting GNSS data from vehicles, which includes latitude, longitude, speed, and heading. Since GNSS data can sometimes be noisy or incomplete due to signal loss, we clean and preprocess it. This step ensures the data is standardized and any missing values are handled effectively, preparing it for the next stages.

**Step 2: Map-Matching Algorithm**
Next, we implement a map-matching algorithm to plot the vehicle’s movement accurately on a map. Here's how it works:

The algorithm takes the raw GNSS data and snaps the coordinates to the nearest road segment on the map.
We use additional factors like vehicle speed, heading, and proximity to known highways or service roads to further refine the matching accuracy.
This ensures that even if the GNSS position is slightly off, our system can still correctly identify which road segment (highway or service road) the vehicle is traveling on.

**Step 3: AI-ML Techniques for Classification**
We then apply machine learning models to make the map-matching smarter. We’ve trained these models on real-world vehicle trajectories, so they can accurately predict whether a vehicle is on the highway or the service road based on the patterns in the data.

The models consider vehicle movement patterns, the structure of the road network, and the behavior of GNSS signals in different environments.
This allows us to handle cases where the GNSS data is unreliable or missing by accurately predicting the vehicle’s position based on historical data.

**Step 4: Handling GNSS Gaps or Biases**
When GNSS data is missing or severely biased, our system uses the following approach:

We analyze the last known position of the vehicle and combine it with the vehicle's average speed and heading to estimate where it is likely to be.
We factor in the road layout and possible routes the vehicle might take, based on its current trajectory, ensuring that the estimate remains accurate even in the absence of live GNSS data.

**Step 5: Integration with GNSS-Based Tolling Systems**
Finally, we integrate this solution into the GNSS-based tolling system. The map-matching and AI-ML algorithms provide precise data on whether a vehicle used the highway or service road, ensuring correct tolls are applied. This makes the tolling system more reliable and fair for users.

**Technology Stack:**

1. Python (Flask): Used to build the backend, handling map-matching, ML model integration, and API development.
2. Node.js/Express.js: Used for frontend server-side scripting and handling user interactions.
3. Amazon SageMaker: For training and deploying our machine learning models.
4. Kafka: For real-time streaming and handling large-scale GNSS data in real-time.
5. PostGIS: For managing geographical data and map processing.
6. OpenStreetMap: Provides digital maps for accurate map matching.
7. AWS (Amazon Web Services): Handles the cloud infrastructure, ensuring scalable and efficient processing and deployment.
8. Scikit-learn and TensorFlow are used for developing and training machine learning models.

### **Model Architecture** 
![archiiiiiiiiiiii](https://github.com/user-attachments/assets/f55d53e0-f79a-444e-bb0a-a32462aecae5)


---

### **Tasks**

🟦 **Problem Understanding & Research**  
   - Research existing map-matching techniques and algorithms.  
   - Understand the challenges of GNSS data, including biases and signal loss.

🟦 **Data Collection**  
   - Gather or simulate GNSS datasets that include vehicle movements on highways and service roads.

🟦 **Data Preprocessing**  
   - Clean and preprocess the GNSS data to handle missing values, noise, and biases.

🟦 **Map-Matching Algorithm Development**  
   - Implement initial map-matching algorithms using geospatial libraries.  
   - Optimize map-matching for distinguishing highway and service road movements.

🟦 **AI-ML Model Development**  
   - Develop and train machine learning models (e.g., classification models) to improve map-matching accuracy.  
   - Experiment with different algorithms (e.g., decision trees, neural networks, clustering techniques).

🟦 **Model Evaluation**  
   - Validate the AI-ML model using a separate dataset.  
   - Evaluate model performance using accuracy, precision, recall, etc.

🟦**Integration & Testing**  
   - Integrate the AI-ML model with the map-matching algorithm.  
   - Test the complete system with different GNSS datasets to ensure robustness.

🟦 **Visualization**  
   - Visualize the vehicle movements on a map and evaluate the algorithm's ability to distinguish between highways and service roads.

🟦 **Documentation**  
   - Document the methodology, algorithms, and results.  
   - Provide a detailed README file to explain project objectives, setup, and usage.

🟦 **Future Enhancements**  
   - Explore potential improvements using advanced AI techniques or real-time processing.
