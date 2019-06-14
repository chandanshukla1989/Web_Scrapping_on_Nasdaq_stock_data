import requests
import csv
import json    

def consolidate_news_csv(ListB):
    for symbol in ListB:
        api_address='https://api.iextrading.com/1.0/stock/'+symbol+'/news'
        url = api_address
        json_data = requests.get(url).json()
        csvfile = open('d:\st_'+symbol+'_news.csv','w',newline='')
        count=0;
        writer = csv.writer(csvfile)
        for item in  json_data:
                if count == 0:
                    writer.writerow(item.keys())
                    count = count+1
                else:
                    writer.writerow(item.values())


    csvfile.close()     
