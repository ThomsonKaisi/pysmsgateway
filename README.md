# pysmsgateway 0.1.0
pysmsgateway is a Python library that provides an interface for sending SMS messages 
    via a gateway using the Traccar SMS Gateway Android application. It allows developers 
    to send SMS messages programmatically from Python code to recipient mobile numbers, 
    using a custom phone number as a reply number to the gateway.

    ### Features:
    - Single SMS sending to a recipient.
    - Bulk SMS sending to multiple recipients.
    - Integration with systems requiring SMS functionality (e.g., 2FA).
    
    ### Important Notice:
    - Download the Traccar Android Application from the playstore.
    - For Local Connection, makesure you are on the same network with the Android phone which has traccar sms gateway application.
    - Go to Settings, collect the IP Address of the phone and the api token.
    - Use the token and the IP and indicated in the example.
    - For more information on traccar sms gateway application to visit [Documentation](https://www.traccar.org/documentation/)
    ### Example Usage:
    ```python
    from pysmsgateway import pysmsgateway

    # Initialize the gateway
    gateway = pysmsgateway(token='your_token', ip='your phone's ip', sms_token='your_sms_token')

    # Sending a single message
    gateway.send_sms('recipient_number', 'Hello, World!')

    # Sending different messages to different recipients
    data = {
        'recipient1': 'Message 1',
        'recipient2': 'Message 2',
        'recipient3': 'Message 3'
    }
    gateway.send_sms_bulk(data)

    # Sending a single message to multiple recipients
    numbers = ['recipient1', 'recipient2', 'recipient3']
    gateway.send_sms_multiple('Single message to multiple recipients', numbers)
    ```
    """,
