# Azure AI Services - Language Detection - REST Client Example

Notes while working through Microsoft's docs and [Learn](https://learn.microsoft.com/) material. Implementation of the REST client from Microsoft.

---

The Azure AI services APIs are designed on a REST architecture, which means that you can interact with them by crafting and sending JSON-formatted requests over the HTTP protocol. This approach provides a flexible and standardized way to communicate with the AI services.

In the example below, we'll provide detailed steps to set up and run a console application that showcases the usage of the Language REST API for language detection. However, it's essential to note that the fundamental approach discussed here is applicable across all APIs supported by the Azure AI Services resource.

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

To install this project, follow these steps:


1. **Clone the Repository:** Begin by cloning the project repository from GitHub. Execute the following command in your terminal or command prompt:

```
git clone https://github.com/brndnsmth/azure-ai-lang-detect-rest-client.git
cd azure-ai-lang-detect-rest-client
```

2. **Environment File Setup:** Create the .env file.

```
touch .env
```

3. **Endpoint and Key:** Add the following, for now:

```
AI_SERVICE_ENDPOINT=YOUR_AI_SERVICES_ENDPOINT
AI_SERVICE_KEY=YOUR_AI_SERVICES_KEY
```

4. **Create a Virtual Environment:** Utilize Python 3 to create a virtual environment for this project. This step ensures a clean and isolated environment for installing dependencies.

```
python3 -m venv .venv
```

5. **Activate the Virtual Environment:** Activate the virtual environment to isolate the project dependencies from other Python installations on your system.

```
source .venv/bin/activate
```

6. **Install Dependencies:** While inside the virtual environment, install the required dependencies specified in the requirements.txt file using pip.

```
pip install -r requirements.txt
```

7. **Configuration Setup:** Update the .env file with your Access Keys and Endpoint. This step is crucial for authenticating requests and accessing the Azure AI services.

8. **Run the Client:** Execute the following command to run the client application:

```
python rest-client.py
```

9. **Input Text:** Follow the prompts provided by the client application. Enter the desired text when prompted for input. This step allows you to test the language detection functionality.
