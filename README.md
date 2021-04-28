# covid-deaths-of-china-japan-france-and-china
from covid import Covid
import covid
import matplotlib.pyplot as plt
import numpy as np

china_cases=Covid().get_status_by_country_name("china")
china_active=china_cases["deaths"]
print(china_active)

japan_cases= Covid().get_status_by_country_name("japan")
japan_active=japan_cases["deaths"]
print(japan_active)

france_cases= Covid().get_status_by_country_name("france")
france_active=france_cases["deaths"]
print(france_active)

australia_cases= Covid().get_status_by_country_name("australia")
australia_active=australia_cases["deaths"]
print(australia_active)

fig = plt.figure()
ax = fig.add_axes([0,0,1,1])
cntry = ['australia', 'china', 'japan', 'france']
num = [australia_active, china_active, japan_active, france_active]
ax.bar(cntry,num)
plt.show()
