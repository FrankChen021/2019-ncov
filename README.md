# 2019-ncov

This repo contains data of daily confirmed cases of 2019 novel coronavirus broken in wuhan China. 

# Data Format

## JSON

The JSON data is something like 


```
{
    //key correpsondes to the name of an administrative area
    "湖北": { 
        "dates":["1-10","1-16","1-17","1-18","1-19","1-20","1-21","1-22","1-23","1-24","1-25","1-26","1-27","1-28","1-29","1-30","1-31","2-1"],
        "data": {
            // accumulated confirmed cases of this province
            "confirmedTotal":9074,
            
            //each element in the arry below correspondes to each date in 'dates' array above
            "dailyConfirmed":[41,4,17,59,77,72,105,69,105,180,323,371,1291,840,1032,1220,1347,1921]
        },
        
        "cities": {
        
            //key correspondes to the name of a city in this administrative area
            "武汉市":{ 
                // accumulated confirmed cases of this city
                "confirmedTotal":4109,
                
                //each element in the arry below correspondes to each date in 'dates' array above
                "dailyConfirmed":[41,4,17,59,77,60,105,62,70,77,46,80,892,315,356,378,576,894]
            },
            
            // next city
        }
    },
    
    // next province
}
```

## CSV Format

The CSV formatted data is much convinent for user to do analysis via some data sheet apps such as Excel.

The basic structure is as below: 

| Province | City | Accumulated Number | 1-10 | 1-16 | 1-17 | ... |
|----------|------|:---:|:--:|:--:|:--:|:--:|
| 湖北      |      | 9074               | 41  | 4    | 17   | 2    |
| 湖北      |  武汉  | 4109 | 41 | 4 | 17 | 9 |

Each row in the CSV table correspondes a province or a city.

# Demo

There's a simple demo to demonstrate the usage of json data. Take a look at http://112.124.202.14/


# Reference

The data are collected from offical report from government daily.

- National Healthy Commission of China
- Healthy Commmissions in 31 provinces of China
 

