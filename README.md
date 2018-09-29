# USAGundeaths
Porject about Gundeaths in USA
import csv
f = open('guns.csv','r')
csvreader = csv.reader(f)
data = list(csvreader)

print(data[:5])
headers = data[:1]
data = data[1:]
print(headers)
print(data[:5])

years = data[1]

year_counts = {}

for row in years:
    if row not in year_count:
        year_count[row] = 1
        
    else:
        year_count[row] = year_count[row] + 1
        
print(year_count)
import datetime
dates = datetime(year = int(data[0]), month = int(data[1]), day = 1)
dates[:5]
date_counts = {}
for row in dates:
    if row not in date_counts:
        date_counts[row] = 1
        
    else:
        date_counts[row] = date_counts[row] + 1
        
date_counts
sex_counts = {}

for row in data[3]:
    if row not in sex_counts:
        sex_counts[row] = 1
    else:
        sex_counts[row] = sex_counts[row] + 1

race_counts = {}

for r in data[5]:
    if r not in race_counts:
        race_counts[r] = 1
    else:
        race_counts[r] = race_counts[r] + 1
        
#So far i have learned how to count the instances of deaths per group we might still have to look at education levels

f = open('census.csv','r')
csvreader = csv.reader(f)
census = list(csvreader)
census

mapping = {'Asian/Pacific Islander':15159516 + 674625,
           'Black':40250635,
            'Native American/Native Alaskan':3739506
            'Hispanic':44618105
             'White':197318956}
race_per_hundredk = {}

for row,bow in race_counts.items():
     race_per_hundredk[bow]= (row/ mapping[bow])*100000
        
race_per_hundredk

intents = data[3]
races = data[7]

homicide_race_counts = {}

for i, race in enumerate(races):
        if race not in homicide_race_counts:
            homicide_race_counts[race] = 0
        if intents[i] == "Homicide":
            homicide_race_counts[race] = homicide_race_counts[race] + 1
            
for row,bow in race_counts.items():
     homicide_race_counts[bow]= (row/ mapping[bow])*100000
        
homicide_race_counts
