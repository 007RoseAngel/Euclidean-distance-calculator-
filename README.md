# Euclidean-distance-calculator-
Phyton ile Öklid Mesafesi 
import math
# Öklid mesafesi hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

# Noktaları tanımlama
points = [(1, 2), (4, 6), (7, 8), (3, 5)]

# Mesafeleri saklayacağımız liste
distances = []

# Her nokta çifti arasındaki mesafeyi hesaplama
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Mesafeler listesini yazdırma
print("Mesafeler:", distances)

# Minimum mesafeyi bulma
min_distance = min(distances)
print("Minimum Mesafe:", min_distance)
