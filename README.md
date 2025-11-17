# Movie Ticket Booking System

A C-based console application for booking movie tickets with advanced data structures implementation.

## About This Project

This program simulates a real-world movie ticket booking system using Hash Maps, Priority Queues, and Linked Lists. Users can browse movies, select venues and time slots, choose seats interactively, and complete bookings with real-time availability tracking.

## Features

- **6 Movies** across different genres (Horror, Drama, Thriller, Comedy, Action, Romantic)
- **Multiple Venues** - 3 cinema locations per movie
- **Time Slots** - Morning, Afternoon, and Evening shows
- **Two Seat Categories** - VIP (20 seats) and Regular (30 seats)
- **Interactive Seat Selection** - Visual seat map with real-time availability
- **Smart Booking** - Prevents double booking using hash-based validation
- **Cancellation Support** - Restore seats if booking is cancelled

## How to Run

### Compile:
```bash
gcc p1.c -o movie_booking
```

### Execute:
```bash
./movie_booking          # Linux/Mac
movie_booking.exe        # Windows
```

## Data Structures Used

1. **Hash Map** - O(1) seat lookup and booking (100 buckets with chaining)
2. **Priority Queue** - VIP bookings processed first
3. **Linked List** - Dynamic time slot management
4. **Structures** - Complex data organization (Movie, Slot, Booking)

## System Specifications

- **Total Seats per Show:** 50 (20 VIP + 30 Regular)
- **Movies Available:** 6
- **Venues per Movie:** 3
- **Time Slots:** 3 per venue
- **Hash Table Size:** 100

## How to Use

1. **Explore Movies** - Browse available movies and genres
2. **Book Tickets:**
   - Select movie
   - Choose venue
   - Pick time slot
   - Select seat type (VIP/Regular)
   - View seat map and choose seats
   - Review and confirm booking

## Available Movies

| Movie | Genre | VIP Price | Regular Price |
|-------|-------|-----------|---------------|
| Smile 2 | Horror | ₹500 | ₹200 |
| Laapataa Ladies | Drama | ₹200 | ₹100 |
| Lucky Baskhar | Thriller | ₹600 | ₹300 |
| Teri Baaton Mein... | Comedy | ₹250 | ₹150 |
| Amaran | Action | ₹150 | ₹100 |
| Mungaru Male | Romantic | ₹350 | ₹200 |

## Code Structure

```c
// Main Components:
- initializeMovies()     // Setup movie data
- Display_Movies()       // Show movie list
- Book_Ticket()          // Handle booking process
- displaySeats()         // Show seat availability
- bookSeats()            // Process seat selection

// Data Structures:
- HashMap                // Seat management
- PriorityQueue          // Booking queue
- Movie struct           // Movie information
- Slot struct            // Time slots (linked list)
```

## Key Functions

- **Hash Operations:** `insertHash()`, `searchHash()`, `deleteHash()`
- **Queue Operations:** `inqueue()`, `outqueue()`
- **Display Functions:** `Display_Movies()`, `display_Slot()`, `displaySeats()`
- **Booking Logic:** `Book_Ticket()`, `bookSeats()`

## Memory Management

- Uses `malloc()` for dynamic allocation
- Proper `free()` calls to prevent memory leaks
- Validates allocation success before use

## Configuration

Modify these constants in the code to customize:

```c
#define MAX_SEATS 50          // Total capacity
#define VIP_SEATS 20          // VIP section size
#define MOVIE 6               // Number of movies
#define SLOT 3                // Time slots per venue
#define MAX_VENUES 3          // Venues per movie
#define Hash_Size 100         // Hash table size
```

## Example Workflow

```
Start → Select Movie (1-6) → Choose Venue (1-3) → 
Pick Slot (1-3) → Enter Seats Count → Choose Type (VIP/Regular) → 
View Seat Map → Select Seat Numbers → Review → Confirm → Done!
```

## Troubleshooting

**Compilation Error:**
```bash
# If gcc not found, install it first
# Linux: sudo apt-get install gcc
# Mac: xcode-select --install
```

**Runtime Issues:**
- Check input is numeric where required
- Ensure seat numbers are within valid range
- Verify sufficient seats available before booking

## Learning Outcomes

This project demonstrates:
- Hash table implementation with collision handling
- Priority queue using linked lists
- Dynamic memory management
- Complex data structure relationships
- Real-world application simulation

---

**Requirements:** GCC Compiler, C99 or higher

**File:** movie_booking.c (2000+ lines)
