import urllib.request as req
import bs4
import pandas as pd
url="https://store.steampowered.com/explore/new/"

request=req.Request(url)
with req.urlopen(request) as reponse:
    data=reponse.read().decode("utf-8")   

root=bs4.BeautifulSoup(data,"html.parser")
titles= root.find_all("div",class_="tab_item_name")
price= root.find_all("div",class_="discount_final_price")
NO = len(titles)

for a in range (0,NO)   :
    Titles = titles[a].string
    Price = price[a].string
    print(Titles,Price)
