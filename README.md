# interactive-data-visualisation
```python
fig = px.scatter(df,
                 x="Total.Number",
                 y='Total.Rate',
                 size='Total.Population',
                 size_max=len(df),
                 hover_name='State',
                 color='State')
fig.update_layout(autosize=False,width=800,height=500)
fig.show()
```
![](./charts/newplot-11.png)


```python
fig = px.bar(max_cases,x='Total.Number',y='State',color_discrete_sequence=['#F83839']*len(max_cases))
fig.update_layout(autosize=False,width=600,height=500)
fig.show()
```
![](./charts/newplot-10.png)

```python
fig = px.bar(max_rates,x='Total.Rate',y='State',color_discrete_sequence=['#FBEE0F']*len(max_rates))
fig.update_layout(autosize=False,width=600,height=500)
fig.show()
```
![](./charts/newplot-9.png)

```python
fig = px.pie(rate_age,values=rate_age.iloc[0,4:],
             names=['Total < 18','Total 18 - 45','Total 45 - 64','Total > 64'],
             width=600,height=300)
fig.show()
```
![](./charts/newplot-8.png)

```python
fig = go.Figure(data=[go.Pie(labels=male.columns[5:],values=male.iloc[0,5:],pull=[0,0.3,0.1,0])])
fig.update_layout(autosize=False,width=600,height=400)
fig.show()
```
![](./charts/newplot-7.png)

```python
fig = go.Figure(data=[go.Pie(labels=['Breast Cancer','Colorectal','Lung Cancer'],
             values=cancer_type.values,hole=.3)])
fig.update_layout(autosize=False,width=600,height=370)
fig.show()
```
![](./charts/newplot-6.png)

```python
fig.layout.margin.update({'t':75, 'l':50})
fig.layout.update({'title': 'Rates of Male vs Rates of Female'})
fig.layout.update({'height':800})
fig.show()
```
![](./charts/newplot-5.png)

```python
fig = px.bar(min_cases,x='Total.Number',y='State',color_discrete_sequence=['green']*len(min_cases))
fig.update_layout(autosize=False,width=600,height=500)
fig.show()
```
![](./charts/newplot-3.png)

```python
fig =go.Figure(go.Sunburst(
    labels=labels,
    parents=parents,
    values=[10]+[round(item,2)/10 for item in list(races)] + r
))
fig.update_layout(margin = dict(t=0, l=0, r=0, b=0))
fig.show()
# Multiply by 10 in all figure shown below to obtain exact value
```
![](./charts/newplot-2.png) 








