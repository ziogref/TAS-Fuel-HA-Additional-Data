# Tasmanian Fuel Prices - Additional Data

This repository holds community-maintained lists of additional data for service stations in Tasmania. This data is used by the [Tasmanian Fuel Prices Home Assistant Integration](https://github.com/ziogref/TAS-Fuel-HA-Intergration) to provide richer, more useful information.

## Purpose

The official FuelCheck API provides fuel prices but does not include details like which stations participate in specific discount programs (e.g., Coles, Woolworths, RACT) or offer amenities like tyre inflation. This repository aims to bridge that gap by crowdsourcing this information from the community.

By contributing, you help all users of the integration get more accurate and useful data in their Home Assistant dashboards.

## Data Structure

The repository is organised into folders based on the type of data. All files use a simple format of one valid station code per line.

#### `/Fuel-Discount/`

Contains lists of stations participating in various fuel discount programs.

* `Woolworths.txt`: Station codes for Ampol and EG Ampol stations that accept the Woolworths discount.
* `Coles.txt`: Station codes for Shell and Coles Express stations that accept the Coles discount.
* `RACT.txt`: Station codes for United and Ampol stations that accept the RACT discount.
* `United.txt`: Station codes for United Petroleum stations that accept their various discount programs.

*Note: The actual discount amounts are configurable in the integration's settings.*

#### `/Tyre-Inflation/`

Contains lists of stations that offer the facilities to inflate your tyres.

* `Sites.txt`: Station codes for locations that have tyre inflation facilities available.

#### `/Distributors/` & `/Operators/`

These folders contain mappings that link a station code to its fuel distributor (e.g., Ampol, Shell) or the company that operates the site. Each file is named after the distributor or operator and contains the station codes they are associated with.

### What is a Station Code?

The "code" is a unique ID from the FuelCheck API for each station. There are two easy ways to find it:

1.  **In Home Assistant**: Add the station as a "Favourite" in the integration's options. The station code will be listed in the sensor's attributes.
2.  **In the FuelCheck Tas App**: Select a station, open its details, and use the "share" button. The shared link will look like `https://fuelcheck.tas.gov.au/app/s/123`, where `123` is the station code.

## How to Contribute

We encourage all users to contribute! If you find incorrect or missing information, you can help by updating the lists.

### The Easy Way: Raise an Issue

This is the best method for most users and requires no technical knowledge.

1.  Go to the [**Issues Tab**](https://github.com/ziogref/TAS-Fuel-HA-Additional-Data/issues) of this repository.
2.  Click **New Issue**.
3.  Give it a clear title (e.g., "Add RACT discount to Ampol Sandy Bay").
4.  In the description, provide the **Station Name**, **Address**, and the **Station Code** if you know it.

### The Advanced Way: Submit a Pull Request

If you are comfortable with GitHub, you can edit the files directly.

1.  **Fork this Repository:** Click the "Fork" button to create your own copy.
2.  **Navigate and Edit:** In your forked repository, find the correct file (e.g., `Fuel-Discount/Coles.txt`) and click the pencil icon to edit it.
3.  **Add the Station Code:** Add the new station code on a new line.
4.  **Commit and Create Pull Request:** Save your change with a brief description and open a pull request to contribute it back to the main project.

Your contribution will be reviewed and, once approved, will benefit all users. Thank you for helping make this project better!
