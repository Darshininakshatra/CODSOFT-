# CODSOFT-
def chatbot_response(user_input):
    user_input = user_input.lower()

    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I assist you today?"
    elif "how are you" in user_input:
        return "I'm fine! how are you?, but I'm here to help you! How can I assist you today?"
    elif "I'm fine!" in user_input:
        return "it's great!"
    elif "what is your name" in user_input:
        return "I'm your friendly chatbot!"
    elif "how can you helph" in user_input:
        return "I can respond to your basic queries. You can try asking me the basic queries you have about time, weather, or any other basic information"
    elif "weather" in user_input:
        return "Sorry! I can't check the weather right now, but you use weather app or check in website for that"
    elif "time" in user_input:
        from datetime import datetime
        return f"The current time is {datetime.now().strftime('%H:%M:%S')}."
    elif "joke" in user_input:
        return "Why can't the bicycle stand up by itself? It was two tired."
    elif "how old are you" in user_input:
        return "as old as internet"
    elif "thankyou" in user_input:
        return "You're Welcome! Let me know if you need more suggestions!"
    elif "Bye" in user_input:
        return "Bye! Have a  great day"
    
def chat():
    print("chatbot: Hello! How can I assist you today?")
    while True:
        user_input = input("You: ")
        if user_input.lower() in ["Bye", "goodbye"]:
            print("chatbot: Goodbye! Have a great day!")
            break
        else:
            response = chatbot_response(user_input)
            print(f"chatbot: {response}")

chat()
