'''
Created on Feb 9, 2018

'''
#############################################
#                                           #
# Don't blame me, I voted for Kodos.        #
#                                           #
#############################################

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

class donationRecipient:
    def __init__(self, recipientID):
        self.recipientID = recipientID #'C0038415' 
        self.recipientZipCode = '02895'
        self.year = 2018
        self.sponsorDonations = [333] #, 384, 200, 1, 1]
        self.sponsorNumbers = [1]  #, 2, 3, 4, 5]
        self.percentileValue =333
    def addDonationAmt(self, sponsorDonation):
        self.sponsorDonations.append(sponsorDonation)    
    def addNumber(self, sponsorNumber):
        self.sponsorNumbers.append(sponsorNumber)      
    textFilePercentile = percentile    

f = open("itcont.txt", "r")
data = f.readlines()
list = []
for line in data:
#    print line 
    lineSplit=line.split('|')
   print lineSplit
    #need take split lines list, assign it to donation recipient by number
    #how do you create new strings, concatonate? see below.    "
f.close()
