#most_frequent2
def fun(y):
    dictionary = {}
    for letter in y:
        dictionary[letter] = 1 + dictionary.get(letter, 0)
    return dictionary
def most_frequent(string):
    letters = [letter.lower() for letter in string if letter.isalpha()]
    dictionary = fun(letters)
    result = []
    for key in dictionary:
        result.append((dictionary[key], key))
    result.sort(reverse=True)
    for count, letter in result:
        print(letter, count)
most_frequent('mississippi') most_frequent2
