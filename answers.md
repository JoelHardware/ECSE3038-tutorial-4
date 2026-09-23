When the post request is made twice it sends two separate entries to the dictionary, hence it is not idempotent (status code 201).

When the put request is made twice the server remains the same as no data changes, hence it is idempotent (status code 200).

When the delete request is made twice the server remains the same as the data cannot be deleted twice, hence it is idempotent (status code 200 for first request then 404 for the second request).