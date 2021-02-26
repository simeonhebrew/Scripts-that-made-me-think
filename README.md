# Scripts-that-made-me-think
Here are some scripts that I hacked after a LOOOOONG time of thinking and debugging :-)


**Finding GC Content in a sequence and displaying degenerate bases and their positions if the sequence is not DNA (Python)**

def percentageGC(sequence):

        "This function calculates the %GC Content in a DNA Sequence"
        GC_Count = sequence.count("G") + sequence.count("C")/len(sequence)*100
        true_DNA = 'ACTG'
        
        
 for base in sequence:
 
            if base not in true_DNA:
              print("There is an invalid base %s at position %d" % (base,sequence.find(base)))
        return GC_Count
        
 **Finding the longest repeats in DNA Sequence**       


 import re

with open ("../Data/sequence.txt") as DNA:

     bases = DNA.read()
     
m = re.search(r"(A+A)",bases)
if m:
    print("Here is the repeat!")
    repeat1 = m.group()
    print("The repeat is" + repeat1)
    print("The length of the repeat is %d" % len(repeat1))
    
    
m = re.search(r"(G+G)",bases)
if m:
    print("Here is the repeat!")
    repeat2 = m.group()
    print("The repeat is" + repeat2)
    print("The length of the repeat is %d" % len(repeat2))
    
    
m = re.search(r"(C+C)",bases)
if m:
    print("Here is the repeat!")
    repeat3 = m.group()
    print("The repeat is" + repeat3)
    print("The length of the repeat is %d" % len(repeat3))
    

m = re.search(r"(T+T)",bases)
if m:
    print("Here is the repeat!")
    repeat4 = m.group()
    print("The repeat is" + repeat4)
    print("The length of the repeat is %d" % len(repeat4))
    
    
