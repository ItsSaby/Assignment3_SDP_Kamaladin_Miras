# **# Assignment #3 — Bridge Pattern**



##### **## Overview**



This project demonstrates the \*\*Bridge Design Pattern\*\* in Java.



The chosen example is a \*\*Shape–Renderer\*\* system. The main idea is to separate the shape itself from the way it is rendered. This allows both sides to change independently.



For example, the same `Circle` can be rendered using either a `VectorRenderer` or a `RasterRenderer`.



##### **## Project Structure**



The project contains two separate hierarchies.



##### **### Shape hierarchy**



\- `Shape` — the main abstraction

\- `Circle` — a concrete shape

\- `Square` — a concrete shape



##### **### Renderer hierarchy**



\- `Renderer` — the implementation interface

\- `VectorRenderer` — vector rendering implementation

\- `RasterRenderer` — raster rendering implementation



`Main` acts as the client and demonstrates how the two hierarchies work together.



##### **## How the Bridge Works**



The main part of the pattern is the relationship between `Shape` and `Renderer`.



`Shape` contains a reference to the `Renderer` interface:



```java

protected final Renderer renderer;


