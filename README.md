# README.md

## List of Commands
- Headings: # H1, ## H2, ### H3
- Bold Text: ** text ** (no spaces between text and *'s)
- Italic Text: * text * (no spaces between text and *'s)
- Blockquotes: > quote
- Ordered List: 1. First Example, 2. Secon Example, 3. Third Example
- Unordered List: same as above but use "-" instead of numbers
- Code: 'code'
- Horizontal Rule: ---
- Link: '[title](https://www.blahblahblah.com)'
- Image: '![text](image.jpg)'

## Code Fencing
'''
{
    # Jack
    ## William
    ### Beaver
}
'''

'''
{
    **Bold Text**
    *Italicized Text*
}
'''

'''
{
    > "This is an example of a blockquote."
}
'''

'''
{
    1. Kansas City Chiefs
    2. Missouri Tigers
    3. Kansas City Royals
    4. Denver Nuggets
}
'''

'''
{
    - Item 1
    - Item 3
    - Item 5
    - Item 2
    - Item 4
}
'''

## Bash Tips
Up Arrow:
The up arrow in Bash brings the last line of code that you ran. If you contine to use the up arrow it continues to scroll through the last couple of lines of code that you ran.

-n Flag:
The -n flag produces a numeric amount of times something is used. For this assignment it brings back the amount of times a word is used.

-r Flag:
The -r flag produces a list in reverse order. For this assignment it brought back the reverse list of the words used in the URL we chose.

Dashes:
There is only one dash used for one letter, however, if the word is two or more letters long then there are two dashes.

## Curl Commands
Curl Command Used to Obtain Data:

curl "https://www.espn.com/nfl/story/_/id/29766900/nfl-rank-predicting-best-100-players-2020-nfl-season" > data.txt

Curl Command Used to Obtain Most Common Words, Sorted:

tr ' ' '\12' < data.txt | sort | unique -c | sort -nr > result.txt

## Commands for Maven, Zookeeper, and Kafka
Open up PowerShell as Administrator from inside the Kafka -version file:

1. Run Zookeeper Service (keep the window open)
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

2. Run Kafka Service (keep the window open)
.\bin\windows\kafka-server-start.bat .\config\server.properties

3. Creates list, topic, or delete topics (temporary window)
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic jacks information
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list

4. Run Kafka Producer to add topics into your list (keep window open)
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic jacks information

5. Run Kafka Consumer (reorders the list)
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic jacks information --from-beginning
