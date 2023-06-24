pip install python-aiml
import aiml
kernel = aiml.Kernel()
kernel.learn("std-startup.xml")
kernel.respond("load aiml b")
while True:
    input_text = input("You: ")
    response = kernel.respond(input_text)
    print("Bot: " + response)
<aiml version="1.0.1" encoding="UTF-8">
    <category>
        <pattern>WHAT IS YOUR NAME</pattern>
        <template>My name is Chatbot.</template>
    </category>
    <category>
        <pattern>WHAT IS THE WEATHER TODAY</pattern>
        <template>I'm sorry, I don't have access to real-time weather information.</template>
    </category>
</aiml>
