# 🎬 Movie Ticket Booking System

A comprehensive C-based console application that simulates a real-world movie ticket booking system with advanced data structure implementation including Hash Maps, Priority Queues, and Linked Lists.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation Guide](#installation-guide)
- [Project Structure](#project-structure)
- [System Architecture](#system-architecture)
- [Usage Guide](#usage-guide)
- [Data Structures](#data-structures)
- [Available Movies](#available-movies)
- [Troubleshooting](#troubleshooting)

## 🎯 Project Overview

The Movie Ticket Booking System is a terminal-based application built in C that demonstrates practical implementation of core data structures and algorithms. The system allows users to browse movies, select venues and time slots, choose seats interactively, and complete bookings with real-time seat availability tracking.

**Key Highlights:**
- Real-time seat availability management
- Priority-based booking system (VIP vs Regular)
- Interactive seat selection interface
- Dynamic queue management for booking requests
- Hash-based seat reservation system

## ✨ Features

### 🎬 Movie Management
- **Multiple Movies**: Browse through 6 different movies across various genres
- **Multiple Venues**: Each movie available at 3 different cinema locations
- **Time Slots**: Multiple showtimes per day (Morning, Afternoon, Evening)
- **Genre Variety**: Horror, Drama, Thriller, Comedy, Action, and Romantic films

### 🎫 Booking System
- **Dual Seating Categories**:
  - VIP Seating: 20 premium seats with exclusive pricing
  - Regular Seating: 30 standard seats for general audience
- **Interactive Seat Map**: Visual ASCII-based seat availability display
- **Real-time Updates**: Instant seat status updates after each booking
- **Collision Prevention**: Prevents double booking of seats
- **Booking Confirmation**: Review and confirm before finalizing

### 🔐 Seat Management
- **Visual Representation**: 'O' for available, 'X' for booked seats
- **Intelligent Validation**: Checks seat availability before booking
- **Booking Cancellation**: Option to cancel and restore seats
- **Seat Number Selection**: Choose specific seat numbers

## 📸 Screenshots

### Main Menu
<img width="625" height="197" alt="Screenshot 2025-11-17 081907" src="https://github.com/user-attachments/assets/8ae09157-72f5-4033-bf51-8a068db66ebc" />


### Movie Selection
<img width="642" height="479" alt="Screenshot 2025-11-17 082131" src="https://github.com/user-attachments/assets/efb3cff4-0093-40e3-8eae-644a3fd413a5" />


### Venue and Time Slot Selection
<img width="800" height="442" alt="Screenshot 2025-11-17 082302" src="https://github.com/user-attachments/assets/ac400338-17ff-48a5-832e-84e6196058de" />


### Interactive Seat Selection
<img width="741" height="485" alt="Screenshot 2025-11-17 111639" src="https://github.com/user-attachments/assets/742bdab9-c740-41d9-8599-f5a781ca09e9" />
<img width="681" height="579" alt="Screenshot 2025-11-17 111729" src="https://github.com/user-attachments/assets/f80771cc-93bf-4c02-bda0-fbf4950e6192" />


### Booking Summary and Confirmation
<img width="774" height="339" alt="Screenshot 2025-11-17 111919" src="https://github.com/user-attachments/assets/e0b97efc-b341-44ce-ba2f-ec3b958b9e2c" />


**Note:** To add screenshots:
1. Create an `images/` folder in your repository
2. Take screenshots while running the program
3. Save them in the `images/` folder with the names shown above
4. Uncomment the image lines by removing `<!--` and `-->`

## 🛠️ Technology Stack

### Core Language
- **C Programming Language** (C99 standard)

### Data Structures
- **Hash Map**: O(1) seat lookup and booking management
- **Priority Queue**: Priority-based booking request handling
- **Linked List**: Dynamic slot and venue management
- **Structures**: Complex data organization for movies, slots, and bookings

### Libraries Used
```c
#include <stdio.h>    // Standard I/O operations
#include <stdlib.h>   // Memory allocation
#include <string.h>   // String operations
#include <ctype.h>    // Character type functions
```

## 📥 Installation Guide

### Prerequisites
- GCC compiler (MinGW for Windows, GCC for Linux/Mac)
- C99 or higher standard support
- Terminal/Command Prompt

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/movie-ticket-booking-system.git
cd movie-ticket-booking-system
```

### Step 2: Compile the Program
```bash
# Using GCC
gcc p1.c -o movie_booking

# On Windows with MinGW
gcc p1.c -o movie_booking.exe
```

### Step 3: Run the Application
```bash
# On Linux/Mac
./movie_booking

# On Windows
movie_booking.exe
```

## 📁 Project Structure

```
movie-ticket-booking-system/
├── p1.c                 # Main source code
├── README.md            # Project documentation
└── movie_booking        # Compiled executable (after compilation)
```

## 🏗️ System Architecture

### Component Diagram
```
┌─────────────────────────────────────────────────────────┐
│              Movie Booking System                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │   Hash Map   │  │ Priority     │  │  Linked      │   │
│  │   (Seats)    │  │   Queue      │  │   List       │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│         │                  │                  │         │
│         └──────────────────┴──────────────────┘         │
│                            │                            │
│                   ┌────────▼────────┐                   │
│                   │  Movie Struct   │                   │
│                   │  - Title        │                   │
│                   │  - Genre        │                   │
│                   │  - Venues       │                   │
│                   │  - Prices       │                   │
│                   │  - Slots        │                   │
│                   └─────────────────┘                   │
└─────────────────────────────────────────────────────────┘
```

### System Flow
```
User Registration → Movie Selection → Venue Selection → 
Slot Selection → Seat Type Choice → Seat Selection → 
Booking Confirmation → Ticket Generation
```

## 📖 Usage Guide

### Main Menu
When you run the application, you'll see:
```
==================================================
Welcome to our Movie ticket booking Program 
==================================================
1. Explore Movies
2. Book the tickets
3. Exit
---------------------------------------------------
```

### Option 1: Explore Movies
- Displays all available movies with their genres
- Browse without making a booking

### Option 2: Book Tickets

#### Step-by-Step Booking Process:

**1. Select Movie**
```
Choose a movie you would love to watch: 1
```

**2. Choose Venue**
```
Available Venues for 'Smile 2': 
1. PVR FORUM MALL
2. Fun Cinemas
3. Manasa Theatre
Choose the venue: 1
```

**3. Select Time Slot**
```
+-----+------------------+-------------------+-------------------+
| Slot | Time             | VIP Seats         | Regular Seats    |
+-----+------------------+-------------------+-------------------+
| 1   | 9:00AM-12:00PM   | 20                | 30               |
| 2   | 2:00PM-5:00PM    | 20                | 30               |
| 3   | 6:00PM-9:00PM    | 20                | 30               |
+-----+------------------+-------------------+-------------------+
Select the slot: 3
```

**4. Enter Number of Seats**
```
How many seats would you like to book? 2
```

**5. Choose Seat Type**
```
VIP Ticket Price: 500
Regular Ticket Price: 200

Pick your perfect spot to enjoy the show!
1. VIP 
2. Regular 
What's your choice? 1
```

**6. View and Select Seats**
```
Available VIP Seats (O = Available, X = Booked):
------------------------------------------------------------
O1   O2   O3   O4   O5   
O6   O7   O8   O9   O10  
O11  O12  O13  O14  O15  
O16  O17  O18  O19  O20  

Enter 2 seat numbers separated by spaces: 5 10
```

**7. Review and Confirm**
```
----------------------------------------------
          Booking Summary                     
----------------------------------------------
 Movie: Smile 2                     
 Venue: PVR FORUM MALL                     
 Slot number: 3                           
 Number of Seats: 2                     
 Total Price: 1000                    
-------------------------------------------------------
Do you want to confirm the booking? yes
```

## 🗂️ Data Structures

### 1. Hash Map Implementation
```c
Purpose: O(1) seat lookup and reservation
Size: 100 buckets
Collision Handling: Chaining method
Operations: Insert, Search, Delete
```

**Key Features:**
- Fast seat availability checking
- Efficient booking and cancellation
- Hash function: `(hash * 31 + char) % 100`

### 2. Priority Queue
```c
Purpose: Manage booking requests by priority
Implementation: Linked list with priority sorting
Priority Levels:
  - 1: VIP bookings (higher priority)
  - 2: Regular bookings (standard priority)
```

**Operations:**
- `enqueue()`: Add booking request
- `dequeue()`: Process highest priority request

### 3. Linked Lists
```c
Purpose: Dynamic slot and venue management
Structure: Movie → Venues → Time Slots
Benefits:
  - Dynamic size
  - Easy insertion/deletion
  - Memory efficient
```

### 4. Structures
```c
- Movie: Stores movie details, venues, pricing, slots
- Slot: Time, available seats per category
- BookingRequest: Complete booking information
- HashNode: Key-value pairs for seat tracking
```

## 🎭 Available Movies

| # | Movie Title | Genre | Venues | VIP Price | Regular Price |
|---|------------|-------|--------|-----------|---------------|
| 1 | Smile 2 | Horror | PVR FORUM MALL, Fun Cinemas, Manasa Theatre | ₹500 | ₹200 |
| 2 | Laapataa Ladies | Drama | AMB Cinemas, Victory Cinemas, Akash Cinemas | ₹200 | ₹100 |
| 3 | Lucky Baskhar | Thriller | Cinepolies, INOX, PVR Cinemas Gold | ₹600 | ₹300 |
| 4 | Teri Baaton Mein... | Comedy | Urvashi Theatre, Everest Theatre, Cauvery Theatre | ₹250 | ₹150 |
| 5 | Amaran | Action | IMAX, S.B.J, The Binge Town | ₹150 | ₹100 |
| 6 | Mungaru Male | Romantic | Pruthvi, Guru, Balaji Cinemas | ₹350 | ₹200 |

### Time Slots (All Movies)
- **Slot 1**: 9:00 AM - 12:00 PM (Morning Show)
- **Slot 2**: 2:00 PM - 5:00 PM (Matinee Show)
- **Slot 3**: 6:00 PM - 9:00 PM (Evening Show)

## 🔧 Technical Specifications

| Component | Specification |
|-----------|--------------|
| Max Seats per Show | 50 (20 VIP + 30 Regular) |
| Total Movies | 6 |
| Venues per Movie | 3 |
| Time Slots | 3 per venue |
| Hash Table Size | 100 buckets |
| Memory Management | Dynamic (malloc/free) |
| Input Validation | Comprehensive checking |

## ⚙️ Configuration

### Modifiable Constants
```c
#define MAX_SEATS 50          // Total seats per show
#define VIP_SEATS 20          // VIP category seats
#define REGULAR_SEATS 30      // Regular category seats
#define MOVIE 6               // Total movies available
#define SLOT 3                // Time slots per venue
#define MAX_VENUES 3          // Venues per movie
#define Hash_Size 100         // Hash table size
```

## 🐛 Troubleshooting

### Common Issues and Solutions

#### Compilation Errors
```bash
# If you get "undefined reference" errors
gcc p1.c -o movie_booking -lm

# If you get "stdio.h not found"
# Ensure GCC is properly installed and in PATH
```

#### Runtime Issues

**Issue**: Program crashes after booking
```c
Solution: Check if memory allocation succeeded
- Verify malloc() returns non-NULL
- Ensure proper free() calls
```

**Issue**: Seats remain booked after cancellation
```c
Solution: Verify deleteHash() function is called
- Check seat restoration logic
- Ensure hash key matches exactly
```

**Issue**: Invalid seat selection accepted
```c
Solution: Add range validation
- Check seat number is between 1 and MAX_SEATS
- Verify seat type (VIP/Regular) boundaries
```

## 📊 Performance Characteristics

| Operation | Time Complexity | Space Complexity |
|-----------|----------------|------------------|
| Seat Lookup | O(1) average | O(n) |
| Booking Request | O(n) worst case | O(1) |
| Slot Traversal | O(n) | O(1) |
| Movie Display | O(n) | O(1) |

## 🎓 Learning Outcomes

This project demonstrates:
- ✅ Practical implementation of Hash Maps
- ✅ Priority Queue usage in real-world scenarios
- ✅ Linked List dynamic memory management
- ✅ Structure-based data organization
- ✅ Input validation and error handling
- ✅ Memory management (malloc/free)
- ✅ Modular code design

---

<div align="center">

**⭐ Star this repo if you found it helpful! ⭐**

Made with ❤️ and C Programming

</div>
