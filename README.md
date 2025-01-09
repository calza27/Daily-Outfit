# Daily-Outfit
Main repo for the Daily Outfit app. Documentation, ideation, and design all kept here.

Supporting repos linked below

## Design Brief
This application is designed to allow users to upload picutres and details of clothes in their wardrobe. Clothes can be tagged with attributes pertaining to the formality of the item (ranging from casual to black tie formal), the type of item and wear it's worn on the body, and the temperature/weather range the item is appropriate for.

Users can then request an outfit for the day, giving the level of formality, and restricting the selection to types of clothes. The application will pull weather forcast data for their local area, or an area of the users choosing, and select items from the users wardrobe to suggest a clothing combination. The selection is made using a random number generator, and users can either "re-roll" the whole selection or individual pieces should the result not be to their liking, or make choices on what items to swap out.

## Tech Stack
The main application will be made available via an adroid and apple application, purchasable from the relevant app stores.

Users will authenticate using username/password or social identity provider, leveraged by Amazon Cognito

This will give a token which will serve as authentication to the API.

An API Gateway will front up Lambda functions written in golang. User metadata, clothing, and confirmed outfits will be stored in DynamoDB, with images being stored in an S3 bucket.

## Supporting Repositories

[Android Application](https://github.com/calza27/DO-Android)

[Apple Application](https://github.com/calza27/DO-Apple)

[Supporting Infrastructure (S3, DynamoDb, Cognito)](https://github.com/calza27/DO-Infra)

[API and Lambdas](https://github.com/calza27/DO-API)
