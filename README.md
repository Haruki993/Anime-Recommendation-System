Here’s your text beautifully formatted as a `README.md` using Markdown syntax:

````markdown
# 🎌 ANIME RECOMMENDER

This recommender is developed using **user-based collaborative filtering** and an **SVM classifier**. The dataset is acquired from **Kaggle**.

The model is trained using up to **1000 users** due to hardware limitations. Despite this, the preprocessed input reaches a dimension of approximately **390,785 x 3,534**, resulting in exported CSV files totaling nearly **±5 GB** in size.

The recommendation system uses **cosine similarity** to find *k* similar users and identifies the top *n* anime based on their scores. An **SVM classifier** then predicts the selected user's *disliked anime* based on genre and removes them from the final recommendation list.

---

## 🚀 Features

- ✅ User-based collaborative filtering with SVM classifier  
- 🌐 Web interface for easy interaction  
- 🖥️ CLI support for direct recommendations  
- 🎭 Genre-based filtering and analysis  
- 📐 Cosine similarity for user matching  
- 📊 Handles large-scale anime dataset  

---

## 🛠️ Setup & Installation

1. **Clone this repo and move to its directory:**
   ```bash
   git clone <repository-url>
   cd anime-recommender
````

2. **Create and activate your virtual environment:**

   ```bash
   python -m venv venv

   # For Windows
   .\venv\Scripts\activate

   # For Linux/Mac
   source venv/bin/activate
   ```

3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🎮 How To Use

### 🌐 Webserver Method

1. **Configure environment variables:**

   ```bash
   cp .env.example .env
   # Then edit .env with your settings
   ```

2. **Start the Flask server:**

   ```bash
   flask run
   ```

3. Open your browser and navigate to:
   **[http://localhost:5000](http://localhost:5000)**

4. Select a user and wait for recommendations to appear.

---

### 💻 CLI Method

1. Follow setup instructions in the `data/` and `export/` directories.

2. **Run the recommender:**

   ```bash
   python recommender.py
   ```

> ℹ️ **Note:** By default, it shows recommendations for user `Zexu` (user\_id: `459521`).
> Edit `recommender.py` to change the target user.

---

## 🔧 Project Structure

```
anime-recommender/
├── app/
│   ├── controller/
│   ├── model/
│   ├── static/
│   └── templates/
├── data/
├── export/
└── recommender.py
```

---

## 🤝 Contributing

Feel free to open **issues** and submit **pull requests** — all contributions are welcome!

---

## 📄 License

This project is open source and available under the **MIT License**.
