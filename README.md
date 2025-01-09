# SPEECH-RECOGNITION-SYSTEM-TASK4

*COMPANY*: CODTECH IT SOLUTIONS
*NAME*: KOPPISETTI THANUSHMA SHIVANI
*INTERN ID*:CT12EGF
*DOMAIN*: EMBEDDED SYSTEMS
*BATCH DURATION*:DECEMBER 17th, 2025 TO FEBURARY 17th, 2025
*MENTOR NAME*:NEELA SANTOSH KUMAR

# DESCRIPTION OF THE TASK

OBJECTIVE:
   The objective of a Speech Recognition System is to enable command-based control of devices through voice input, providing a hands-free and intuitive user interface. This system leverages speech recognition technology to process spoken commands, interpret them, and trigger corresponding actions on connected devices. Implemented using an embedded board, it demonstrates the practical application of voice control in modern automation. The system aims to enhance user convenience, improve accessibility, and reduce reliance on physical controls, making it suitable for smart home applications, industrial automation, and assistive technologies.

INTRODUCTION:
  A Speech Recognition System is an innovative technology designed to enable devices to interpret and respond to spoken commands. By building a basic speech recognition system, users can control devices seamlessly using their voice, eliminating the need for physical interaction. This system, implemented with an embedded board, processes audio input, converts it into text or commands, and triggers the corresponding actions on connected devices. It represents a significant step towards creating intuitive and accessible human-machine interfaces, finding applications in smart homes, assistive technologies, and industrial automation. This system demonstrates the potential of voice-based control in enhancing user convenience and interaction.

KEY ACTIVITIES:
1.Audio Input Capture:
Use a microphone to capture spoken commands.

2.Signal Processing:
Convert the captured audio signals into a digital format for processing by the embedded board.

3.Speech Recognition:
Use a speech recognition module or software to analyze and recognize the spoken words or commands.

4.Command Interpretation:
Interpret the recognized commands into actionable instructions.

5.Device Control:
Trigger corresponding actions on the connected devices based on the recognized commands.

6.Calibration:
Fine-tune the system to accurately recognize specific commands or keywords.

7.Power Management:
Ensure stable power supply and efficient operation of the embedded system.

8.System Integration:
Integrate the embedded board with the devices for seamless control and communication.

9.Communication Protocols:
Set up communication channels (e.g., Bluetooth, Wi-Fi) between the embedded system and devices.

SOURCE CODE:
import speech_recognition as sr

def speech_to_text():
    # Initialize recognizer
    recognizer = sr.Recognizer()

    # Use the microphone as the audio source
    with sr.Microphone() as source:
        print("Adjusting for ambient noise... Please wait.")
        recognizer.adjust_for_ambient_noise(source, duration=1)
        print("Listening for your speech...")

        try:
            # Capture audio input
            audio = recognizer.listen(source, timeout=5, phrase_time_limit=10)
            print("Processing audio...")

            # Recognize speech using Google Web Speech API
            text = recognizer.recognize_google(audio)
            print("You said:", text)
            return text

        except sr.UnknownValueError:
            print("Sorry, I could not understand the audio.")
        except sr.RequestError as e:
            print(f"Could not request results from the recognition service; {e}")
        except Exception as e:
            print(f"An error occurred: {e}")

if _name_ == "_main_":
    speech_to_text()

CIRCUIT DIAGRAM:https://github.com/minukurinavya/SPEECH-RECOGNITION-SYSTEM-TASK4/commit/392bc092a7117ae6f647ca410174a36943cafbb5

BLOCK DIAGRAM:https://github.com/minukurinavya/SPEECH-RECOGNITION-SYSTEM-TASK4/commit/ffbc589b8acf533500417cc693b1fb617290a6c6

 WORKING:
    The Speech Recognition System operates by capturing spoken commands through a microphone, which serves as the audio input. The embedded board processes these audio signals, converting them into a digital format suitable for analysis. A speech recognition module or algorithm on the board interprets the digital audio, identifying specific keywords or phrases that correspond to predefined commands. Once the commands are recognized, the system translates them into control signals that trigger actions on connected devices, such as turning a light on or off or adjusting a thermostat. This process occurs in real time, ensuring seamless and efficient device control. Additional features, like noise filtering and keyword detection, enhance the system's accuracy and reliability, making it a practical solution for hands-free command-based automation.

CONCLUSION:
  In conclusion, the Speech Recognition System provides a practical and efficient solution for command-based control of devices using voice input. By integrating a microphone, embedded board, and speech recognition technology, the system enables seamless and hands-free operation, enhancing user convenience and accessibility. Its ability to interpret spoken commands and execute corresponding actions in real time demonstrates its potential in smart automation, assistive technologies, and industrial applications. This system highlights the power of voice-controlled interfaces in creating intuitive and interactive environments, paving the way for future advancements in human-machine interaction.


OUTPUT OF THE PROJECT:https://github.com/minukurinavya/SPEECH-RECOGNITION-SYSTEM-TASK4/commit/6b0776a3b1ce1facf79a87bcb56dca8d0803a938
