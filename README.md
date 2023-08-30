- 👋 Hi, I’m @Franken44
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Franken44/Franken44 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from flask import Flask

app = Flask(__name__)

@app.route("/")
def index():
    """Generates a flowchart from the given code."""

    code = """
import matplotlib.pyplot as plt

# Define the steps of the process
steps = ["Isolasi gen cryA1 dari bakteri Bacillus thuringiensis",
         "Kloning gen cryA1 ke vektor pembawa",
         "Transformasi vektor pembawa ke sel kapas",
         "Seleksi tanaman kapas transgenik",
         "Pengujian tanaman kapas transgenik untuk ketahanan terhadap hama",
         "Produksi benih kapas transgenik"]

# Define the start and end points
start = (0, 0)
end = (10, 0)

# Define the coordinates of the steps
coordinates = []
for i in range(len(steps)):
    coordinates.append((i * 2, 0))

# Plot the arrows
for i in range(len(steps) - 1):
    plt.arrow(coordinates[i], coordinates[i + 1], head_width=0.1, head_length=0.1)

# Add the labels
for i in range(len(steps)):
    plt.text(coordinates[i], steps[i], fontsize=10)

# Add the title
plt.title("Pembuatan Kapas Bt")

# Show the plot
plt.show()
