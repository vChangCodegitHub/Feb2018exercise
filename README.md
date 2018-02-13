'''
Created on Feb 9, 2018

'''
#############################################
#                                           #
# Don't blame me, I voted for Kodos.        #
#                                           #
#############################################

percentile = 0
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

DR_C0038415_2018 = donationRecipient('C0038415')
DR_C00629618_2017 = donationRecipient('C00629618')
DR_C00177436_2017 = donationRecipient('C00177436')
#DR_C00177436_2017.recipientID = 'C00177436'
DR_C00384516_02895_2017 = donationRecipient('C00384516')
DR_C00384516_02895_2017 = donationRecipient('C00384516')
DR_C00384516_02895_2017.sponsorDonations.append(384)
DR_C00384516_02895_2017.sponsorNumbers.append(2)
DR_C00384818_2017=donationRecipient('C00384818')

#print "|%s|%s" %(DR_C00384818_2017.recipientID, DR_C00384818_2017.recipientZipCode)
#print "|%d" %DR_C00384818_2017.year

listOfDonationRecipients=[DR_C00629618_2017, DR_C00177436_2017, DR_C00384818_2017, DR_C00384516_02895_2017]        
#print donationRecipient.sponsorNumber
print (listOfDonationRecipients[0].recipientID, listOfDonationRecipients[0].sponsorNumbers)
print (listOfDonationRecipients[3].recipientID, listOfDonationRecipients[3].sponsorNumbers)
listOfDR_useful=[]
listLength=len(listOfDonationRecipients)
print "List length is %d" %listLength
for i in range(listLength):
    if len(listOfDonationRecipients[i].sponsorNumbers)>1:
        print "donation recipient %s has more than 1 member"\
            %(listOfDonationRecipients[i].recipientID)
        listOfDR_useful.append(listOfDonationRecipients[i])
print listOfDR_useful[0].sponsorDonations
#need to modify below so if more than 1 element listOfDruseful, can do this, result in nested for loop
#calculate greatest rank percentile value
listOfDR_useful[0].percentileValue= \
    greatestRank(percentile, len(listOfDR_useful[0].sponsorDonations),\
                  listOfDR_useful[0].sponsorDonations)
print listOfDR_useful[0].percentileValue

total_donation=0
