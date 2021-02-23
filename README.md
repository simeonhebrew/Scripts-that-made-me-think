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
