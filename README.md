# QuickEats: Salesforce Food Redistribution Platform
![QuickEats Homepage Screenshot](HomePageScreenshot.png)

**QuickEats** is a Salesforce-based application designed to address the dual challenges of global food waste and local hunger. It provides an organized and efficient platform for food redistribution, connecting food donors (like restaurants and hotels) with organizations serving the underprivileged (like NGOs and community kitchens).

Leveraging Salesforce's automation and CRM capabilities, the system simplifies the donation process, optimizes logistics, and provides real-time tracking to ensure surplus food reaches those in need promptly.

## Core Features & Technical Components

This project is a demonstration of a complete Salesforce build, from data model to user interface. The configuration includes:

* **Data Model:**

  * **Standard Objects:** Utilizes `Account`, `Contact`, and `Case` to manage donor/NGO relationships and track issues.

  * **Custom Objects:** A complete custom data model to manage the redistribution process:

    * `Venue`: Stores information on food source locations (restaurants, event sites).

    * `Dropoff Point`: Captures details of recipient locations (shelters, NGOs).

    * `Volunteer`: Tracks volunteer details, availability, and assignments.

    * `Task`: Manages specific actions needed for the redistribution (e.g., schedule pickup).

    * `Execution Details`: Holds logistical information for the actual delivery.

* **User Interface (UI/UX):**

  * **Lightning App:** A dedicated "QuickEats" Lightning App with a custom navigation bar.

  * **Custom Tabs:** Tabs for all major custom objects for easy access.

  * **Custom Homepage:** A custom-designed homepage featuring key reports and a "Venue Form" flow for quick data entry.

* **Automation:**

  * **Salesforce Flow:** A Screen Flow ("Venue Form") guides users through the process of adding a new food donation venue.

  * **Apex Trigger:** A `before insert` trigger (`DropOffTrigger`) on the `Drop_Off_Point__c` object automatically calculates and populates distance fields.

* **Security & Sharing:**

  * **Custom Profiles:** A custom "NGOs Profile" created to grant specific object and field permissions to end-users.

  * **Public Groups:** Groups created (e.g., "Iksha") to manage record sharing.

  * **Sharing Rules:** Criteria-based sharing rules on the `Drop-Off point` object automatically share records based on distance, ensuring the right teams have visibility.

* **Analytics:**

  * **Custom Report Types:** Created to join `Venues`, `Drop-Off Points`, and `Volunteers` for comprehensive analysis.

  * **Reports:** Built reports like "venue and Drop Off point" and "Volunteer Task" to track logistics and performance.

  * **Dashboard:** A central "Organization Details" dashboard to visualize key metrics and operational data in real-time.

## Project Author

* **Vatsal Unadkat**

* `vatsalunadkat07@gmail.com`
