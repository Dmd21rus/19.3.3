import requests
import json

# Make a GET request to the /pet/findByStatus endpoint with query parameter status=available
response = requests.get('https://petstore.swagger.io/v2/pet/findByStatus', params={'status': 'available'})
print(response.json())

# Make a POST request to the /pet endpoint to add a new pet
new_pet = {'name': 'Fluffy', 'photoUrls': [], 'status': 'available'}
response = requests.post('https://petstore.swagger.io/v2/pet', json=new_pet)
print(response.json())

# Make a PUT request to the /pet endpoint to update an existing pet
updated_pet = {'id': 1, 'name': 'Fluffy', 'photoUrls': [], 'status': 'sold'}
response = requests.put('https://petstore.swagger.io/v2/pet', json=updated_pet)
print(response.json())

# Make a DELETE request to the /pet endpoint to delete an existing pet
response = requests.delete('https://petstore.swagger.io/v2/pet/1')
print(response.json())
