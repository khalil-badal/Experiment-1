# EMOTICON PROBLEM: Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon:

 
# Start


def replace_words_with_emoticons(sentence):
    
    # Define a dictionary that maps words to emoticons
    emoticons = {
        'smile': ':)',
        'grin': ':D',
        'sad': ':(',
        'mad': '>_<'
    }
    
    # Split the sentence into a list of words
    words = sentence.split()
    
    # Create a new list to store the replaced words
    new_words = []
    
    # Loop through each word in the list
    for word in words:
        # If the word is in the dictionary, replace it with the emoticon
        if word in emoticons:
            new_words.append(emoticons[word])
        else:
            # If the word is not in the dictionary, keep it as is
            new_words.append(word)
    
    # Join the list of words back into a single string
    new_sentence = ' '.join(new_words)
    
    return new_sentence

def main():
   
    # Ask the user to enter a sentence
    user_sentence = input("Please enter a sentence: ")
    
    # Call the function to replace words with emoticons
    result_sentence = replace_words_with_emoticons(user_sentence)
    
    # Display the result
    print("Sentence with emoticons:", result_sentence)

# Call the main function
main()

# End
