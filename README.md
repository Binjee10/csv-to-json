# cvs-to-json

"""13.Write a CSV-to-JSON translator that expects a path to a CSV file as argument, and for each line, 
prints out a JSON object encapsulating that record. """

# Function to convert a CSV to JSON
# Takes the file paths as arguments
def csvtojson(csvFilePath):
    file = open(csvFilePath, "r")
    
    # Open a csv reader called DictReader
  dict_reader = csv.DictReader(file)
    
    # Creating a dictionary from csv contents
    # use the json.dumps() function to dump data
  dict_from_csv = list(dict_reader)[0]
  json_from_csv = json.dumps(dict_from_csv)
    
  print(json_from_csv)
    
# Decide the two file paths according to your
# computer system
csvFilePath='Sample.csv'

csvtojson(csvFilePath)
