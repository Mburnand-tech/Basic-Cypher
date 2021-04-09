# Basic-Cypher
My first Github. A Caesar Cypher which inputs a decoded message and an agreed offset. 


def Vishal_decode(message, offset):
    Decoded_message = ""
    for words in message:
        for letters in words:
            if Alphabet.find(letters) != -1:
                Original_position = Alphabet.find(letters)
                Decoded_position = Original_position + offset
                if Decoded_position > len(Alphabet):
                    over_variable = Decoded_position - len(Alphabet)
                    New_letter = Alphabet[over_variable]
                    Decoded_message += New_letter
                if Decoded_position < len(Alphabet) + 1: 
                    New_letter2 = Alphabet[Decoded_position - 26]
                    Decoded_message += New_letter2
            if Alphabet.find(letters) == -1:
                Decoded_message += letters
    
    return print(Decoded_message)
