CDN Server with Movie Searcher
This project is a Content Delivery Network (CDN) server designed to efficiently distribute and display movie images. Developed in C++ and Qt for the GUI, this application provides a responsive interface where users can view popular movie images or search for specific ones based on their location.

Table of Contents
Project Structure
Features
Setup
Usage
Classes and Components
Future Improvements
Project Structure
The project is organized into the following components:

WelcomeWindow: Displays the initial interface, collects user coordinates.
ResultsPage: Shows movie images based on user location, enables search, and updates based on the nearest CDN node.
CDNManager: Handles main server management, CDN nodes, movie requests, and storage of popular movies.
Movie: Represents a movie object, including properties like name and poster image.
CDNNode: Represents individual CDN nodes with coordinates and a cache of popular movies.
MainServer: Central repository for all movies.
Features
Location-Based Image Display:

Displays movie images from the CDN node closest to the user’s location.
Movie Search:

Users can search by movie name. If found, the image and details are displayed.
Grid Layout Display:

Movies are shown in a dynamic 3x3 grid, adjusting based on available data.
CDN Node Management:

The CDNManager class handles node operations, storing popular movies and ensuring efficient retrieval.
Setup
Prerequisites
Qt Framework: Download and install the Qt Framework from the following link for GUI support:
bash
Copy code
https://www.qt.io/download-dev#eval-form
C++ Compiler: Requires a compiler compatible with C++11 or newer.
Filesystem Library: Requires C++17 for file handling.
Important Notes
Network Requirement: For optimal performance and stability, connect via LAN instead of WiFi when running the application.
Steps to Download and Set Up the Project
Clone the Repository:

bash
Copy code
git clone https://github.com/OmChandraSharma/CDN_Optimization.git
Open All Project Files in Qt Creator:

Launch Qt Creator and open all the files within the CDN_Optimization folder at once to ensure all dependencies and components are loaded correctly.
Build the Project:

In Qt Creator, select Build to compile the project.
Run the Project:

Once built, click Run to start the application and open the GUI for the CDN Server with Movie Searcher.
Usage
Initial Setup

Start the application, which will open the Welcome Window.
Enter your coordinates (X and Y between 0 and 200) and submit. This is used to calculate the nearest CDN node.
Viewing Movie Images

The ResultsPage displays movie images based on the user’s location.
Popular movies from the nearest CDN node are shown in a 3x3 grid layout.
Search for a Movie

Enter the movie name in the search bar to search across CDN nodes.
If the movie is found, its image and details are displayed.
Classes and Components
WelcomeWindow

Collects and validates user coordinates, connects inputs to ResultsPage.
ResultsPage

Displays images from the nearest CDN node and provides a search bar.
CDNManager

Manages CDN nodes, retrieves popular movies efficiently.
CDNNode
Represents a node with (x, y) coordinates and stores nearby popular movies.
Movie
Defines movie properties, including name and image path.
MainServer
Central repository for movies, manages image paths for retrieval.

Future Improvements
Dynamic Node Allocation
Allow CDN nodes to adjust their cache based on recent user requests.
Improved Search Functionality
Add fuzzy matching for more flexible search results.
Enhanced Image Caching
Apply advanced caching for frequently accessed images to boost performance.