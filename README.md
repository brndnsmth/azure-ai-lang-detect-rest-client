# Azure AI Services - REST Client Example

## Provision an Azure AI Services Resource

To begin, follow these steps:

1. **Access Azure Portal:** Navigate to [Azure Portal](https://portal.azure.com) and sign in using your Microsoft account associated with your Azure subscription.
  
2. **Create Azure AI Services Resource:**
    - In the search bar at the top, look for "Azure AI services" and select the corresponding option.
    - Proceed to create a new Azure AI services multi-service account resource with the following specifications:
        - **Subscription:** Your Azure subscription
        - **Resource group:** Choose or create a resource group (if your subscription is restricted, you might need to use a provided resource group)
        - **Region:** Choose any available region
        - **Name:** Enter a unique identifier
        - **Pricing tier:** Standard S0
        - Check the required checkboxes and proceed to create the resource.

3. **Deployment Completion:** Wait for the deployment process to finish, and then review the deployment details.

4. **Access Keys and Endpoint:**
    - Navigate to the resource and locate the "Keys and Endpoint" page.
    - Here, you'll find crucial information necessary for connecting to your resource and utilizing it within your applications, including:
        - An HTTP endpoint for client applications to send requests.
        - Two authentication keys (either of which can be used by client applications for authentication).
        - The hosting location of the resource, essential for certain API requests (though not all).

By following these steps, you can efficiently set up and utilize Azure AI Services resources within your applications.


## REST Client Setup

The Azure AI services APIs operate on a REST architecture, allowing you to interact with them by sending JSON requests via HTTP. In the following example, we'll delve into a console application utilizing the Language REST API for language detection. However, the underlying principle remains consistent across all APIs supported by the Azure AI Services resource.

To install this project, follow these steps:

1. Clone the repository from GitHub using the following command:

```
git clone https://github.com/brndnsmth/azure-ai-rest-client.git
```

2. Create a virtual environment using Python 3:

```
python3 -m venv .venv
```

3. Activate the virtual environment:

```
source .venv/bin/activate
```

4. Once in virtual environment (.venv), install the backend dependencies using pip:

```
pip install -r requirements.txt
```

5. Run the client

```
python rest-client.py
```

6. When prompted for some text, try entering some text.