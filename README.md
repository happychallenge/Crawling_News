# Crawling_News

import re
import requests

url = 'http://news.joins.com/article/21453330'
html = requests.get(url).text

result = re.sub(r'<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>', '', html)
print(result)
