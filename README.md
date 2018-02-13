'''
Created on Feb 9, 2018

'''
#############################################
#                                           #
# Don't blame me, I voted for Kodos.        #
#                                           #
#############################################

output_length=2
percentile = 20
#function returning value corresponding to percentile greatest rank
def greatestRank(percentile, numListMem, inputList): 
    ordinalNum = 1 + (percentile*numListMem/100)
    print ordinalNum
    greatestRankValue = inputList[ordinalNum - 1]
    return greatestRankValue

f = open("percentile.txt", "r")
percentile = f.read()
percentile = float(percentile)
f.close()
print "percentile is %s" %percentile

    
