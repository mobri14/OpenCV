# OpenCV
OpenCV


ENGLISH Comments:

```import cv2

# Load the face detection model
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

# Start capturing video from the default camera
cap = cv2.VideoCapture(0)  # 0 for the default camera

while True:
    # Read frames from the camera
    ret, frame = cap.read()
    
    if not ret:
        break
    
    # Detect faces in the color image
    faces = face_cascade.detectMultiScale(frame, scaleFactor=1.1, minNeighbors=5)
    
    # Draw rectangles around detected faces
    for (x, y, w, h) in faces:
        cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

    # Display the image with detected faces
    cv2.imshow("Face Detection", frame)

    # Press 'q' to exit the loop
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Release the video capture and destroy all windows
cap.release()
cv2.destroyAllWindows()
```



Spanish Comments:

```
# Cargar el modelo de detección de caras
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

# Iniciar la captura de video desde la cámara predeterminada
cap = cv2.VideoCapture(0)  # 0 para la cámara predeterminada

while True:
    # Leer los fotogramas de la cámara
    ret, frame = cap.read()
    
    if not ret:
        break
    
    # Detectar caras en la imagen en color
    faces = face_cascade.detectMultiScale(frame, scaleFactor=1.1, minNeighbors=5)
    
    # Dibujar rectángulos alrededor de las caras detectadas
    for (x, y, w, h) in faces:
        cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

    # Mostrar la imagen con las caras detectadas
    cv2.imshow("Detección de Caras", frame)

    # Presiona 'q' para salir del bucle
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Liberar la captura de video y destruir todas las ventanas
cap.release()
cv2.destroyAllWindows()
```
French  Comments:

```
# Charger le modèle de détection de visage
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

# Commencer à capturer la vidéo depuis la caméra par défaut
cap = cv2.VideoCapture(0)  # 0 pour la caméra par défaut

while True:
    # Lire les images de la caméra
    ret, frame = cap.read()
    
    if not ret:
        break
    
    # Détecter les visages dans l'image couleur
    faces = face_cascade.detectMultiScale(frame, scaleFactor=1.1, minNeighbors=5)
    
    # Dessiner des rectangles autour des visages détectés
    for (x, y, w, h) in faces:
        cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

    # Afficher l'image avec les visages détectés
    cv2.imshow("Détection de Visage", frame)

    # Appuyez sur 'q' pour quitter la boucle
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Libérer la capture vidéo et détruire toutes les fenêtres
cap.release()
cv2.destroyAllWindows()
```

German Comments:

```
# Das Gesichtsdetektionsmodell laden
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

# Videoaufnahme von der Standardkamera starten
cap = cv2.VideoCapture(0)  # 0 für die Standardkamera

while True:
    # Bilder von der Kamera lesen
    ret, frame = cap.read()
    
    if not ret:
        break
    
    # Gesichter im Farbbild erkennen
    faces = face_cascade.detectMultiScale(frame, scaleFactor=1.1, minNeighbors=5)
    
    # Rechtecke um die erkannten Gesichter zeichnen
    for (x, y, w, h) in faces:
        cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)

    # Bild mit erkannten Gesichtern anzeigen
    cv2.imshow("Gesichtserkennung", frame)

    # Drücken Sie 'q', um die Schleife zu verlassen
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Videoaufnahme freigeben und alle Fenster schließen
cap.release()
cv2.destroyAllWindows()
```
