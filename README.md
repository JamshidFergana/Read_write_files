import re

def main():
    r = r'My name is .*\.'
    r1 = r'My name is (.*)\.'
    
    match = re.match(r, "My name is Jamshid.")
    match1 = str(re.findall(r1, "My name is Jamshid."))
    print('Name is ', bool(match), match)
    print('Name is ', bool(match1), match1)
    
main() 
