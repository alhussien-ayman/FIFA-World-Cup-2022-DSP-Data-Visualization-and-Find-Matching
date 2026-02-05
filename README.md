# FIFA World Cup 2022 - DSP Data Visualization 


<div align="center">
<img src="static/LOGO.png" alt="HumSearch Logo" width="120" height="120"/>


<br/>
<br/>

**Discover similar plays using advanced Digital Signal Processing algorithms!**

<br/>

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

<br/>


<p align="center" style="display:flex; align-items:flex-start; gap:10px;">
  <img src="static/Photos/FIFA_Screen-01.png" alt="HumSearch Interface" width="25%" />
  <img src="static/Photos/Fifa-02.png" alt="HumSearch Results" width="40%" />
  <img src="static/Photos/Fifa-03.png" alt="HumSearch Results" width="40%" />
</p>>
</div>

---

## 📖 About

FIFA World Cup 2022 - DSP Data Visualization is a sophisticated platform that combines advanced Digital Signal Processing algorithms with interactive web technologies to analyze and visualize football match data. Built with Django and powered by state-of-the-art similarity search algorithms, it enables users to discover tactically similar plays and goal sequences from the FIFA World Cup 2022.

Ever wondered which goals had similar buildup patterns? Or which plays shared the same tactical execution? This platform solves these challenges by applying DTW (Dynamic Time Warping) and TF-IDF semantic analysis to football event data, revealing hidden patterns in the beautiful game.

### Why FIFA DSP Visualization?

- ⚽ **Advanced Analytics** - leverage DSP algorithms for football analysis
- 🔍 **Multi-dimensional Search** - find similar plays using spatial and semantic matching
- 🎨 **Interactive Visualization** - explore matches on a dynamic pitch canvas
- 📊 **Goal Sequence Analysis** - automatically extract and analyze goal buildup patterns
- 🚀 **High Performance** - optimized data loading with singleton caching architecture

---

## ✨ Features

- 🏆 **Match Exploration** - Browse comprehensive metadata, rosters, and key events from World Cup 2022
- ⚽ **Goal Sequence Extraction** - Automatically captures crucial events preceding every goal
- 🔍 **DTW Similarity Search** - Find plays with similar spatial and temporal patterns using FastDTW
- 📝 **TF-IDF Semantic Search** - Discover plays with similar event types and tactical patterns
- 🎯 **Hybrid Search Engine** - Combined scoring system merging DTW and TF-IDF for optimal accuracy
- 🎨 **Interactive Pitch Rendering** - Visualize player formations and ball trajectories
- 📊 **Formation Analysis** - Examine player positioning and spatial relationships
- 🌐 **Real-time Updates** - Dynamic loading of match events and sequences
- 📱 **Responsive Design** - Optimized for desktop, tablet, and mobile viewing
- ⚡ **High-Performance Caching** - Singleton DataLoader for instant data access

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+**
- **pip** (Python package manager)
- Modern web browser (Chrome, Firefox, or Edge)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/DSPFINALFIFA-MAIN.git
cd DSPFINALFIFA-MAIN
```

2. **Create a virtual environment** (recommended)
```bash
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

3. **Install Python dependencies**
```bash
pip install django numpy scikit-learn fastdtw
```

4. **Verify data files are present**
```bash
# Ensure FIFA_datan directory contains:
# - Metadata.json
# - Events.json
# - Rosters.json
```

5. **Run migrations**
```bash
python manage.py migrate
```

6. **Start the development server**
```bash
python manage.py runserver
```

7. **Open your browser** and navigate to `http://localhost:8000`

---

## 💻 Usage

### 🎯 Match Exploration

1. Navigate to the **Match Browser**
2. Select a match from the FIFA World Cup 2022
3. View comprehensive match metadata and team rosters
4. Explore key events chronologically

### ⚽ Goal Sequence Analysis

1. Click on any **Goal Event** in the match timeline
2. View the automatically extracted buildup sequence
3. Examine the events leading up to the goal
4. Visualize the play on the interactive pitch

### 🔍 Similarity Search

**DTW Search (Spatial Similarity)**
1. Select a goal sequence or play
2. Click **Find Similar Plays (DTW)**
3. View results ranked by spatial and temporal similarity
4. Compare ball movements and player formations

**TF-IDF Search (Semantic Similarity)**
1. Select a goal sequence or play
2. Click **Find Similar Plays (TF-IDF)**
3. View results ranked by event type and tactical patterns
4. Analyze similar play structures

**Hybrid Search (Best of Both)**
1. Select a goal sequence or play
2. Click **Hybrid Search**
3. Get the most accurate matches combining both algorithms
4. Explore plays that are both spatially and semantically similar

### 💡 Tips for Best Results

- **Use longer sequences** - 5+ events provide better matching accuracy
- **Compare similar match contexts** - open play vs set pieces
- **Adjust similarity thresholds** - fine-tune to balance precision and recall
- **Combine search methods** - hybrid search offers the most comprehensive results
- **Examine pitch zones** - spatial patterns reveal tactical similarities

---

## 📁 Project Structure

```
DSPFINALFIFA-MAIN/
├── FIFA_datan/              # Raw JSON data files
│   ├── Metadata.json        # Match metadata and basic info
│   ├── Events.json          # Detailed event data
│   └── Rosters.json         # Team and player information
├── static/                  # Static assets
│   ├── css/                 # Stylesheets
│   ├── js/
│   │   ├── app.js          # Main application logic
│   │   └── pitch.js        # Pitch visualization engine
│   └── images/             # Icons and graphics
├── templates/               # Django templates
│   └── index.html          # Main application interface
└── DSPFinalFIFA/           # Django project root
    ├── FIFA/               # Main application
    │   ├── DTW.py         # Dynamic Time Warping implementation
    │   ├── TF_IDF.py      # TF-IDF semantic search
    │   ├── views.py       # HTTP endpoints and API
    │   ├── models.py      # Domain models (Match, Team, etc.)
    │   └── urls.py        # URL routing
    ├── settings.py         # Django configuration
    └── wsgi.py            # WSGI application
```

---

## 🔧 How It Works

### Data Processing Pipeline

1. **Data Loading & Caching**
   - Singleton DataLoader loads JSON files into memory
   - High-performance caching for instant access
   - Normalized data structures for efficient querying

2. **Goal Sequence Extraction**
   - Identifies goal events in match timeline
   - Extracts preceding events (typically 5-10 events)
   - Captures spatial and temporal context
   - Associates player and team information

3. **Feature Extraction**
   - **Spatial Features**: Ball coordinates, player positions, formations
   - **Temporal Features**: Event timing, sequence duration
   - **Semantic Features**: Event types, outcomes, pitch zones
   - **Tactical Features**: Pass types, pressure levels, player roles

4. **Similarity Algorithms**

   **DTW (Dynamic Time Warping)**
   - Calculates Euclidean distance between ball positions
   - Applies event type penalties for mismatches
   - Analyzes player formation similarity
   - Uses FastDTW for optimized performance
   - Returns normalized distance scores

   **TF-IDF Semantic Search**
   - Converts plays into "sentences" of events
   - Maps coordinates to pitch zone descriptors
   - Vectorizes event sequences using scikit-learn
   - Calculates cosine similarity between plays
   - Returns semantic similarity scores

   **Hybrid Search**
   - Combines DTW and TF-IDF scores
   - Weighted scoring system (configurable)
   - Normalizes results across both algorithms
   - Returns comprehensive similarity rankings

5. **Visualization**
   - Renders plays on interactive pitch canvas
   - Displays player formations and movements
   - Shows ball trajectory and event markers
   - Real-time updates with smooth animations

### Technologies Used

- **Backend**: Django (Python)
- **DSP Algorithms**: FastDTW, NumPy, SciPy
- **Machine Learning**: scikit-learn (TF-IDF Vectorization)
- **Frontend**: Vanilla JavaScript, HTML5 Canvas
- **Data Format**: JSON
- **Visualization**: Custom pitch.js rendering engine

---

## 🎓 Technical Deep Dive

### DTW Implementation Details

The Dynamic Time Warping algorithm compares sequences by:

1. **Ball Position Similarity**
   - Euclidean distance: `√((x₁-x₂)² + (y₁-y₂)²)`
   - Normalized to pitch dimensions (0-100 scale)

2. **Event Type Matching**
   - Penalty system for mismatched events
   - Event groups: Pass, Cross, Clearance, Shot, etc.
   - Configurable penalty weights

3. **Formation Analysis**
   - K-nearest neighbors algorithm
   - Average player distance calculations
   - Spatial density metrics

4. **Path Alignment**
   - FastDTW optimization for O(N) complexity
   - Dynamic programming approach
   - Warping path visualization

### TF-IDF Implementation Details

The semantic search system works by:

1. **Document Creation**
   - Each play = one document
   - Events concatenated into sequences
   - Pitch zones mapped to descriptors

2. **Vectorization**
   - TfidfVectorizer from scikit-learn
   - N-gram analysis (1-3 grams)
   - Term frequency normalization

3. **Similarity Calculation**
   - Cosine similarity between vectors
   - Range: 0 (completely different) to 1 (identical)
   - Ranked by descending similarity

4. **Zone Mapping**
   ```
   Pitch divided into 9 zones:
   - def_left, def_center, def_right
   - mid_left, mid_center, mid_right
   - att_left, att_center, att_right
   ```

---

## 🎯 Use Cases

- **Tactical Analysis**: Identify recurring patterns in goal sequences
- **Scouting**: Find similar plays executed by different teams
- **Coaching**: Study successful attacking patterns
- **Research**: Analyze spatial and temporal patterns in football
- **Fan Engagement**: Discover hidden connections between iconic goals
- **Performance Analytics**: Compare team and player effectiveness

---

## 👥 Team

- **Alhussien Ayman**
- **Mohamed Elsayyed Attallah**
- **Abdullah Khalefa**
- **Ahmed Elshinawy**

> Built with ⚽ and 💻 as a collaborative DSP project

---
