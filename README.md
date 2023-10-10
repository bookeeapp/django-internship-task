# Gym Management System API

You are tasked with creating a CRUD API for a gym management system using Django REST Framework. The API should allow users to manage gyms, trainers, clients, and workout sessions. The models should have appropriate relationships between them.

## Requirements

### Gym Model:
- **Fields:**
  - Name (*CharField*)
  - Address (*TextField*)
- Define appropriate methods and properties.

### Trainer Model:
- **Fields:**
  - Name (*CharField*)
  - Specialization (*CharField*)
  - Gym (*OneToOneField: Gym*)
- Define appropriate methods and properties.

### Client Model:
- **Fields:**
  - Name (*CharField*)
  - Age (*IntegerField*)
- Define appropriate methods and properties.

### WorkoutSession Model:
- **Fields:**
  - Client (*ForeignKey: Client*)
  - Trainer (*ForeignKey: Trainer*)
  - Date (*DateField*)
  - Duration (*IntegerField*)
- Define appropriate methods and properties.

## API Endpoints

- `/gyms/`: CRUD operations for gyms.
- `/trainers/`: CRUD operations for trainers.
- `/clients/`: CRUD operations for clients.
- `/workouts/`: CRUD operations for workout sessions.

## Task

### Model Implementations
- Implement the Gym, Trainer, Client, and WorkoutSession models based on the provided requirements.
- Ensure that appropriate relationships (1:1 and 1:n) are established between the models.

### Serializers
- Create serializers for each model (*GymSerializer, TrainerSerializer, ClientSerializer, WorkoutSessionSerializer*) to handle data validation and conversion to/from JSON.

### API Views
- Implement API views using Django REST Framework's ModelViewSet.
- Define appropriate queryset and serializer classes for each view.

### API Endpoints
- Configure the API URLs to include CRUD operations for gyms, trainers, clients, and workout sessions.
- Ensure that the API URLs are named appropriately.

### Documentation
- Create API documentation describing the available endpoints, request/response formats, and authentication (if any).

### Authentication and Permissions (Brownie Points)
- Implement appropriate authentication mechanisms (e.g., token-based authentication) for the API.
- Configure permissions to restrict access to certain API endpoints based on roles (e.g., only trainers can modify workout sessions).

### Handling Edge Cases
- Implement error handling and ensure appropriate HTTP status codes and error messages are returned for various scenarios (e.g., invalid input, non-existent resources).

### Postman Collection
- Create a Postman collection that includes requests for all the API endpoints.
- Share the Postman collection for testing and validation of the implemented API.

## Evaluation Criteria

- Correctness and completeness of the API implementation.
- Proper usage of Django models, serializers, and views.
- Proper handling of relationships (1:1 and 1:n).
- Code readability, organization, and adherence to best practices.
- Well-documented API, including clear and accurate API documentation.
- Proper authentication and authorization mechanisms.
- Handling of edge cases and robust error handling.
- Sharing a Postman collection for ease of testing the API endpoints.

In this analogy, the Gym represents the blog platform, Trainers are analogous to Authors, Clients are analogous to Users, and WorkoutSessions are analogous to Posts. The relationship between Trainer and Gym represents the 1:1 relationship, and the relationship between Client and WorkoutSession represents the 1:n relationship. 
