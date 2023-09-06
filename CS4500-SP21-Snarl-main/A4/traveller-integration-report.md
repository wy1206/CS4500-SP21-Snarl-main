TO: Manager </br>
FROM: Minghao Yu, Yuan Wang </br>
DATE: 02/05/2021 </br>
SUBJECT: Road Feedback on network implementation

The code we get back from the other team followed our specification for the most part. In our specification, we asked for three functions, create_towns(), place_char() and is_unblocked. For those functions, they followed our type definition strictly, as for the arguments that we didn’t specify the type, they gave the definition and implemented the function based on that and we think it satisfies our expectation of the implementation. The only function they added to the implementation is is_valid_town() and it checks if a town has valid properties which we think it’s necessary and should be added to our specification earlier.

Based on the implementation, we think we are able to integrate the code with our client module. Once the server receives the requests, we would write a helper function in the server to pass the argument into the corresponding function. However, for some of the functions, we might change them to adapt the data structure (e.g. In their code, based on our specification, the town network is a dictionary of town name, neighbor list, and character list, but on the client side it was defined as a dictionary of towns and names as pairs to represent the road.) Similar actions are required for other functions, once we ensure the inputs are correct and the logic of the code is correct as well, the server will store the data received and send corresponding responses to the client.

When we were writing our specification, we made a big mistake. We thought that for languages like Python, we don’t have to be strict with the type of our data, so we just gave them a brief data definition without type in details and let the other team decide how to implement it. If we have a chance to improve our specification, we would consider adding the constraints so the other team can implement it step by step without doing that extra work that we are supposed to do. Also, we didn’t think carefully about what other functions we need. The only three functions we have are all based on the description of the assignment. We also realized that we didn't think about what other functions might the other team need when trying to implement the function we asked for. Thus, to improve the specification, we should also consider the intermediate steps we should do to get the main functions to work. By doing that, it will make our specification more structuralized and it would also be more convenient for the developer to follow.