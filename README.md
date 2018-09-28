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

## Depositor
### Overview
The Depositor's job is to get CloudCoins from outside of the program and bring them into the import folder. This may mean getting CloudCoins from a "Deposit" folder on the desktop; scanning new emails for CloudCoins or checking a Communications Broker to see if it has recieved CloudCoins. 
### Events
Phase one: The Depositor will start when the user tells it to check the Communication Broker for new coins. The user may have an account on ComBroker or access the Coins anonymously. 

Phase two: The Depositor will be able to notice if a user drops CloudCoins into a desktop folder. It will be able to look through emails and other things.  
### Details
The Depositor must use the "Receivel 
### Configuration
If the Depositor is to access the ComBroker anonymously, it must have a CloudCoin in its "Keys" folder that it will use as a access token. The Depositor will first need to use the key to get tickets from the RAIDA. Then it can use the tickets to download any coins.  


### 


## Echoer

## Unpacker

## Authenticator

## Grader

## Lossfixer

## FrackFixer

## ShowCoins

## Gallerist

## Minder

## Vaulter

## Exporter

## Emailer

## Transfere

## PayForwarder

## DirectoryMonitor

## Backuper

## Translator

# GUI Servants

## Console

## Window

## Celebrium

## WebService

## PhysicalDetection

# Reports

# Configuration Files

# Logs



