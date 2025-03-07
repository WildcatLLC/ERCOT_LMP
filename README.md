# ERCOT_LMP
Jupyter Notebook to Download and Process Historical LMPs by Node in ERCOT

### Getting Started

1. Register for API Access at: https://developer.ercot.com/applications/pubapi/user-guide/registration-and-authentication/
2. Copy your USERNAME, PASSWORD AND SUBSCRIPTION_KEY in a .env file in the main director
3. Install the pre-requisites in requirements.txt

### Selecting Time and Bus Parameters

1. In Cell 9, set your desired time range:

    "postDatetimeFrom": "2024-01-01"
    "postDatetimeTo": "2024-12-31"

2. In Cell 23, set your desired electricalBuses:

    "allowed_buses = ['AMOCOOIL_CC1','AMOCOOIL_CC1']"

### Run Order

1. Make sure to run cell 3,5 and 7 to Intialize and Establish an API Connection
2. Run remaining cells in order thereafter 
3. If you get timed out by the API Authorization (3600 seconds), then you can simply re-run Cell 7 or call the function get_ercot_token()
4. starting_index = 0 in Cell 17 can be adjusted if a batch run is interupted or if you need to re-start mid run
5. Cell 19 is optional and for troubleshooting/if certain docIds of the batch dataset are missing

### Feel Free to Comment/Contribute