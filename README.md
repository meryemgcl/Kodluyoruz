# Kodluyoruz
import math

# Noktaları tanımlama
points = [(1, 2), (3, 4), (5, 6), (7, 8)]

# Öklid mesafesi hesaplama fonksiyonu
def euclideanDistance(point1, point2):
    return math.sqrt((point1[0] - point2[0])**2 + (point1[1] - point2[1])**2)

# Mesafeleri hesaplama ve saklama
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Minimum mesafeyi bulma ve yazdırma
min_distance = min(distances)
print("Minimum mesafe:", min_distance)
