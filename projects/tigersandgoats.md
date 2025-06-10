---
layout: project
type: project
image: img/vacay/vacay-square.png
title: "Tigers and Goats"
date: 2025
published: true
labels:
  - Neural Networks
  - Machine Learning
  - C++
summary: "Project centered around building/training neural networks."
---

<img class="img-fluid" src="../img/vacay/vacay-home-page.png">

Tigers and Goats is a project designed to introduce students to Neural Networks. Neural Networks are essentially the framework which allows artificial intelligence (AI) to learn. Implementing reinforcement learning into our code allows for our programs to determine the best course of action to take after running thriugh it's trial period.  

Here is some example code to illustrate what functions the Neural Network was trained on:

Loss function: Cross entropy loss for classification
criterion = nn.CrossEntropyLoss()
optimizer = optim.Adam(model.parameters(), lr=0.001)

Train the model
num_epochs = 5
for epoch in range(num_epochs):
    running_loss = 0.0
    for inputs, labels in trainloader:
        inputs, labels = inputs.to(device), labels.to(device)
        optimizer.zero_grad()
        outputs = model(inputs)
        loss = criterion(outputs, labels)
        loss.backward()
        optimizer.step()

        running_loss += loss.item()
    
    print(f"Epoch {epoch+1}/{num_epochs}, Loss: {running_loss/len(trainloader)}")
