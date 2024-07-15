# Take Home Test Challenge for QA Engineers

This is a basic ASP.NET Core Web API for querying mobile food trucks in [San Francisco](https://data.sfgov.org/Economy-and-Community/Mobile-Food-Facility-Permit/rqzj-sfat/data). The API allows users to search for food trucks by name, street, and location. It also includes a Swagger UI for API documentation and very basic testing.

## The Challenge

You will have these challenges:

Part of the QA engineer's work is analyzing the product, identifying areas of significant failure, and defining/acting on priorities. Consider that the testing role also involves demonstrating the value of a good QA strategy and how it benefits the company.

Your goal is to create tests for this application. You can create any unit, integrated, e2e tests, and other necessary tests. When developing tests for the application, it's important that you provide clear explanations for your choices and reasoning for defining priorities and generating tests. This responsibility and accountability are integral to the QA process.

### How we review

We use this criteria to review:

- You don't need to make any changes to the code or fix any bugs, but feel free to report them.
- We will assess the quality of your test cases and the reasoning behind them.
- For automated tests, we will evaluate their coverage, quality, and efficiency.

### What to send back to our team

When done, please send an email back to your point of contact with a compressed (zip) file of your Github project repo. For explaining about the tests, feel free to add to a document of your choice and send it alongside the zip file.

## Project Documentation

This is a very simple API built with ASP.NET Core Web API and SQLite. At startup, the app checks if the database is already created. If not, it will create a SQLite database and insert the CSV file contents into a table to be used on the API.

### Running the Application

There are a few options to run the application. Check 2 examples below.
**Note:** Due to how the application is built, it might take a while for it to run on the first start.

#### Running Locally

The pre-requisites are:

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)

Steps:

1. Clone the repository
2. Build and run the application with:

      ```console
      dotnet build
      dotnet run --project api
      ```

3. Access the API at <http://localhost:5000> and Swagger UI at <http://localhost:5000/swagger>.

#### Docker

1. Build the Docker image with

    ```console
    docker build -t foodftrucksapi .
    ```

2. Run the Docker container:

    ```console
    docker run -d -p 5000:5000 --name foodtrucks-container foodftrucksapi
    ```

3. Access the API at <http://localhost:5000> and Swagger UI at <http://localhost:5000/swagger>.
