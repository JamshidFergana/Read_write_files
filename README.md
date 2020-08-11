import sys

def read_file(filename):
    print('Reading file with read_file()')
    try:
        f = open(filename)
        content = f.read()
        f.close()
    finally:
        print('Finale')
    
    return content    

def way_better(filename):
    print('Reading file with way_better()')
    with open(filename) as f:
        return f.read()

def write_to_file(filename, content, mode='w'):
    with open(filename, mode=mode) as f:
        f.write(content)

    
if __name__ == '__main__':
    print(read_file('txt.txt'))
    print(way_better('txt.txt'))
    
    write_to_file('txt.txt', 'New line\n')
    write_to_file('txt.txt', 'New line\n', mode='a')
