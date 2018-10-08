# Architecture
There are "Best Practices" for diagramming the Architecute of an application so this uses a novel approach that is called "Servant based architecture."  To show how things work, we pretend that there are a lot of people who are shuffling paper around. 

The folder structure is designed to never change. 

The "Servants" and the work that they do are designed to be flexible and changable. 

It is possible to add more Servants as new features are developed. 

There are a few rules about servants. 
  #Servants are containers of code. 
  #Servants are completely decoupled from other servants and do not share code. If you change the code of one servant, it has no effect on the code of others. 
  #Servants can be written in different languages. Therefor Servants create a kind of distributed system. 
  #Some Servants sit and watch a folder. When something changes in that folder they spring to life and go to work. 
  #Some Servants watch command folders. These are folders that outside entities put orders into. The Servant will fill the order. 
  #Some Servants have configuration files that they can read. Generally, all the Servants can read from the same configuration file and only read the part that is applicable to them. 
  #Some Servants talk to outside data stores like the RAIDA and email servers. 
  #Almost all Servants write to log files.
  #Many Servants create reports that are read by other Servants. 


# Servants

## Receiver

The reciever is more like a service and is covered under the CloudBank V2 protocol. 

When the files are added to the folder, a process will check the ticket of each coin AN and if it is good, it will change the status part of the file name to "authentic".
Once a few seconds go by, the Com Broker will put all the authentic parts together into a stack file. The stack file will incude a "pown" value. All authentic ANs get a "p". If an AN is missing, it gets a "f" for fracked. 
The CB will then check to see if it has the account addressed within its' accounts folders. If if does it will move the coin into the grading folder for the grading process to take place. Otherwise it will leave the CloudCoin in the account name folder that is in the Partial folder. 
Each time


## Depositor
### Overview
The Depositor's job is to get CloudCoins from outside of the program and bring them into the import folder. This may mean getting CloudCoins from a "Deposit" folder on the desktop; scanning new emails for CloudCoins or checking a Communications Broker to see if it has recieved CloudCoins. 
### Events
Phase one: The Depositor will start when the user tells it to check the Communication Broker for new coins. The user may have an account on ComBroker or access the Coins anonymously. 

Phase two: The Depositor will be able to notice if a user drops CloudCoins into a desktop folder. It will be able to look through emails and other things.  
### Details
The Depositor must use be able to 
### Configuration
If the Depositor is to access the ComBroker anonymously, it must have a CloudCoin in its "Keys" folder that it will use as a access token. The Depositor will first need to use the key to get tickets from the RAIDA. Then it can use the tickets to download any coins.  

### Reports
The Depositor must 
### Logs


## Echoer

## Unpacker

## Authenticator

## Grader

## Lossfixer
 
SometimesDuring the pounding proces The raiderReturnsNo response.In this caseIt Is unknownWhether the radarUpdated the a.m. with the PamOr not.If a substantial number of radarDo not respondThen the coin is considered lost.Loss fixerWe'll use informationFrom theClaim before it wasSent to the radarAnd the claim after was that's the raterTo see WhichNumberIs in the rater.So the lost fixerMust checkThe a.m.And the PamTo seeWhich one is correct.Once the loss fixtureFigures out. Which number is in the raiderthe coin d tohtcan e bank folde.r be t 

## FrackFixer

## ShowCoins

## Gallerist

Some cloudCoins are associated with custom JPEG's. These CloudCoins become Celebriutm. When cloudCoins are placed into the bank folder, The Gallerist will go to work and check them to see if they have images associated with them. If so, The Gallaerist download the jpes and associated meta data and puts it in the Gallery folder. 

## Minder
The job of the Minder is to allow CloudCOins to be stored in mind. It also allows coins stored in mind to be put bank in the bank. The minder requires the user to supply two passphrases and from the passphrases it creats new ANs for the coins and changes them on the raida. Then it deletes the coins on the local drive but saves the serial number in the Mind folder. 

## Vaulter
The Vault is a folder that is theft resistant. The CloudCoins here have number that if used would not work. The vaulter takes the CloudCoins from the bank and a password from the user. It then adds the password to the second octet of the AN. This makes the CloudCoin unusable. Then, when the person wants to spend them,it will prompt for the password and the password is suptrackted from the octet in the AN putting it back to its original state. 

## Exporter

## Emailer

## Transfere

## PayForwarder
Payforward takes coins from the PayForward Folder and sends them to the RAIDA using the PAY Foward protocol. The raida will then create it own PANs and send them to the specified Communications Broker which is built into the Depositor. This allow transfers to go from person to person without using email. 



## DirectoryMonitor
This process goes to the Diretory and downloads the DNS names that are primary, secondary and tertiariy. These names then can be used to find the RAIDA. 


## Backuper
This process exports all the coins in the bank, fracked folder, Vault and Gallery into a stack file. This can be saved in another location in case someone loses coins. 


## Translator
The translator reads the logs and places the information into the Main Status Report. The Main status report is used by GUIs. The Translater may change the langauge that the GUI will use by translating the outcome. 

# GUI Servants
These GUI programs generate commands and place them in command folders. It also sets configuraion files. Then, it monitors the Master Status Report to see if anything changes. When changes happen, it updates itself to show the user the changes. 


## Console

## Window

## Celebrium

## WebService

## PhysicalDetection

# Reports

# Configuration Files

# Logs



