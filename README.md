<html>
    <head>
        <link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css" />
        <script defer src="https://pyscript.net/latest/pyscript.js"></script>
    </head>
    <body>
        <py-script>
            input_num = input("컴퓨터의 메시지: \n")
            words = [int(input_num[i:i+8]) for i in range(0, len(input_num), 8)]
            word_list = []
            speech = ""
            for num in words:
                word_list.append(bytes.fromhex(hex(num).lstrip('0x')).decode())
            for word in word_list:
                speech = speech + word
            print(speech)
        </py-script>
    </body>
</html>
