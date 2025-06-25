# **Tasmanian Fuel Prices - Additional Data**

This repository holds community-maintained lists of additional data for service stations in Tasmania, such as which stations participate in discount programs or offer certain amenities. This data is used by the [Tasmanian Fuel Prices Home Assistant Integration](https://github.com/ziogref/TAS-Fuel-HA-Intergration) to provide richer, more useful information.

## **Purpose**

The official FuelCheck API does not provide certain details, such as which service stations participate in specific discount programs (e.g., Coles, Woolworths) or offer amenities like tyre inflation. This repository aims to bridge that gap by crowdsourcing this information from the community.

By contributing, you help all users of the integration get more accurate and useful data in their Home Assistant dashboards.

## **Data Structure**

The repository is organized into folders based on the type of data:

### **/Fuel-Discount/**
This folder contains lists of stations participating in various fuel discount programs.
* [cite_start]`Woolworths.txt`: Contains station codes for Ampol and EG Ampol stations that accept the Woolworths 4c/L discount[cite: 3].
* [cite_start]`Coles.txt`: Contains station codes for Shell and Coles Express stations that accept the Coles 4c/L discount[cite: 2].
* [cite_start]`RACT.txt`: Contains station codes for United, and Ampol stations that accept the RACT 6c/L discount[cite: 4].

*Note: Fuel discount amounts are configurable in the integration's settings.*

### **/Tyre-Inflation/**
This folder contains lists of stations that offer specific amenities.
* [cite_start]`Sites.txt`: Contains station codes for locations that have tyre inflation facilities available[cite: 1].

The format for all files is simply one valid station code per line.

### **What is a Station Code?**

The station "code" is a unique identifier provided by the FuelCheck API for each service station. The easiest way to find the code for a specific station is to add it as a "Favourite Station" in the Tasmanian Fuel Prices integration options and check its attributes.

Alternatively, in the FuelCheck Tas app, you can select a station, open its details page, and use the "share" button. The shared link will look like this `https://fuelcheck.tas.gov.au/app/s/123`, where `123` is the station code.

## **How to Contribute**

We encourage all users to contribute! If you know of a station that has a feature or discount that isn't listed, you can help by adding it. The easiest way to contribute is by submitting a Pull Request.

### **Steps to Contribute**

1.  **Fork this Repository:** Click the "Fork" button in the top-right corner of this page to create your own copy of this repository.
2.  **Navigate to the Correct File:** In your forked repository, find the file corresponding to the data you want to add (e.g., `Fuel-Discount/Coles.txt`).
3.  **Edit the File:** Click the pencil icon to edit the file.
4.  **Add the Station Code:** Add the new station code on a new line at the end of the file. Please only add one code per line.
5.  **Commit the Change:** Scroll to the bottom, provide a brief description of your change (e.g., "Add Coles Express Hobart station to Coles.txt"), and save the change.
6.  **Create a Pull Request:** Go back to the main page of your forked repository. You should see a banner prompting you to "Contribute" and "Open a pull request". Click this button, review your changes, and submit the pull request.

Your contribution will be reviewed and, once approved, will be added to the main list for all users to benefit from. Thank you for helping make this project better!
