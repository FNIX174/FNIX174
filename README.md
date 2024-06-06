# Define a function for the AI conversation
def ai_conversation(user_input):
    # Define some basic responses
    greetings = ["pheonix"]
    farewells = ["over"]

    # Convert user input to lowercase for case-insensitive matching
    user_input = user_input.lower()

    # Check if user input matches any greetings
    if user_input in greetings:
        return "copy! on stand by"

    # Check if user input matches any farewells
    elif user_input in farewells:
        return "over!"
    
    # If no matches, respond with a default message
    else:
        return "nothing located or found try somthing else commander"

# Main loop for the conversation
while True:
    # Get user input
    user_input = input("You: ")

    # End the conversation if the user says goodbye
    if user_input.lower() in ["goodbye", "bye", "see you later", "take care"]:
        print(ai_conversation(user_input))
        break

    # Get AI response
    response = ai_conversation(user_input)

    # Print AI response
    print("AI: " + response)
