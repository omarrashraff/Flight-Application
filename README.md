# ✈️ Flight & Passenger Management System

Developed in collaboration with @minshawi0 as part of the Cryptography course at Cairo University, Faculty of Engineering.

A C++ Object-Oriented Programming project that models an airline flight and passenger management system. Built to demonstrate core OOP concepts including operator overloading, copy constructors, static members, and dynamic passenger management.

> Built for an OOP course project.

---

## Overview

This system allows users to register passengers, assign them to flights, search for seats, and manage passenger counts dynamically. It showcases a rich set of overloaded operators on both the `flight` and `passenger` classes, and uses a static member to track the global passenger count across all objects.

---

## Features

- Add passengers to a flight dynamically via user input
- Display available flights with their number and destination
- Copy a flight object using the copy constructor
- Search for a specific seat and row on a flight
- Add and remove passengers using overloaded operators
- Track total passenger count globally using a static class member
- Display detailed flight and passenger information

---

## Class Structure

```
Flight-Passenger-System/
├── main.cpp          # Entry point — input loop, operator demos, seat search
├── flight.h / .cpp   # flight class: flight number, destination, capacity, passengers
└── passenger.h / .cpp # passenger class: name, seat; static total passenger counter
```

### Classes

**`passenger`**
- Stores passenger name and seat number
- Static member `totalpassengers` tracks count across all instances
- Overloaded `>>` for input and `display()` for output

**`flight`**
- Stores flight number, destination, and passenger list
- Overloaded operators: `+=`, `-=`, `++`, `--`, `<<`
- Copy constructor for deep copying flight objects
- `displayflightdetails()` for formatted output
- `searchforseatnumer(seat, row)` for seat lookup

---

## Concepts Demonstrated

| Concept | Where Used |
|---|---|
| Operator Overloading | `+=` adds passenger, `-=` removes, `++`/`--` increment/decrement flight, `<<` for output, `>>` for input |
| Copy Constructor | `flight fL2(fL1)` — deep copies flight with all passengers |
| Static Members | `passenger::gettotalpassengers()` tracks count globally |
| Dynamic Input Loop | `do-while` loops for adding/removing passengers |
| Seat Search | `searchforseatnumer(seat, row)` searches assigned seats |
| Encapsulation | Getters like `getflightnumber()`, `getdestination()` |

---

## Available Flights

The system includes three predefined flights:

| # | Flight Number | Destination | Capacity |
|---|---|---|---|
| 1 | 205 | Paris | 100 |
| 2 | 215 | Switzerland | 120 |
| 3 | 250 | Italy | 135 |

---

## How to Run

### Prerequisites
- A C++ compiler supporting C++11 or later (e.g. `g++`, `clang++`)

### Compile

```bash
g++ -o flight_system main.cpp flight.cpp passenger.cpp
```

### Run

```bash
./flight_system
```

### Sample Interaction

```
Welcome! Please enter your info.
[Enter passenger name and seat]
Do you want to add more passengers? (Y/N): Y
...

Available flights:
1. Flight number: 205 to Paris
2. Flight number: 215 to Switzerland
3. Flight number: 250 to Italy

Displaying passengers' details:
...

Current passenger count: 3

Enter the seat you want to search for: 5
Enter the row you want to search for: 2
Do you want to search for another seat? (Y/N): N
```

---

## Authors

> OOP Course Project
