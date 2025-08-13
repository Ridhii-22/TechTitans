# TechTitans
# Savya - EODB Navigator

Savya is a single-page web application designed to simplify the process of understanding business compliance requirements in Delhi, India. It provides a user-friendly interface for entrepreneurs to quickly identify the licenses and government schemes relevant to their specific business sector.

The application features an interactive wizard that personalizes a dashboard based on user input, aiming to make the "Ease of Doing Business" (EODB) more accessible.

![Savya EODB Navigator Screenshot]("C:\Users\ridhi\OneDrive\Pictures\Screenshots\Screenshot 2025-08-13 103512.png")


---

## Features

-   *Interactive Landing Page:* A visually appealing landing page with a gradient background and a clear call-to-action.
-   *Business Information Wizard:* A step-by-step form that collects essential details about the user's business.
-   *Dynamic Dashboard Generation:* Based on the wizard's input, the application dynamically generates a personalized dashboard showing required licenses and recommended schemes.
-   *AI Compliance Assistant (UI Mockup):* A section designed for future integration of an AI-powered assistant.
-   *Responsive Design:* Built with Tailwind CSS to ensure it works well on all screen sizes.
-   *Modern Glassmorphism UI:* The "glass card" effect gives the application a clean, modern look.

---

## How to Use

1.  *Clone the repository or download the code:*
    bash
    git clone https://github.com/your-username/savya-eodb-navigator.git
    
2.  *Navigate to the project directory:*
    bash
    cd savya-eodb-navigator
    
3.  **Open the index.html file:**
    -   Simply open the index.html file in any modern web browser (like Chrome, Firefox, or Edge).

4.  *Start the Wizard:*
    -   On the landing page, click the *"Create My Roadmap in 2 Minutes"* button.

5.  *Provide Business Details:*
    -   Select your primary business sector and check any other applicable boxes.
    -   Click the *"Generate My Dashboard"* button.

6.  *View Your Personalized Dashboard:*
    -   The application will display a dashboard tailored to your selections, showing required licenses and recommended schemes.

---

## Technologies Used

-   *HTML5:* For the structure and content.
-   *Tailwind CSS:* A utility-first CSS framework for rapid UI development.
-   *JavaScript (ES6):* For handling user interactions, DOM manipulation, and dynamic content generation.
-   *Font Awesome:* For scalable vector icons.
-   *Google Fonts:* For the "Poppins" font.

---

## Code Overview

The application's logic is self-contained within a single index.html file.

### HTML Structure

-   The <body> is divided into three main <section> tags:
    1.  #landingPage: The initial view.
    2.  #wizard: The form for collecting user data.
    3.  #dashboard: The section where personalized results are displayed.
-   A sticky <nav> bar remains at the top for branding and navigation.

### CSS Styling

-   *Tailwind CSS* is used for almost all styling, linked via a CDN.
-   A small <style> block in the <head> contains custom CSS for:
    -   .gradient-bg: The animated gradient background.
    -   .glass-card: The "glassmorphism" effect.
    -   .hidden-section & .visible-section: Classes to control the single-page transitions.

### JavaScript Logic

-   The entire script is contained within a <script> tag at the end of the <body>.
-   *DOM Element Selection:* Key elements are selected and stored in constants.
-   **showSection(section):** A function that manages which section is currently visible.
-   *Event Listeners:*
    -   An event listener on the startWizardBtn transitions the view to the wizard.
    -   A submit event listener on the wizardForm captures user input and calls the dashboard generation function.
-   **db object:** A simple in-memory JavaScript object acts as a database, holding the data for licenses and schemes and their requirement rules.
-   **generateDashboard(selections):** This core function filters the db object based on user selections and uses template literals to dynamically generate the HTML for the dashboard cards.
