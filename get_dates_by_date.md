# Get all date by day of a month

```php
    function get_dates(){
        $first_day = date('Y-m-01');
        $day_count = date('t');
        $date_by_day = [];
        for ($i = 1; $i <= $day_count; $i++) {
            $date = date('Y/m').'/'.$i;
            $date = date('Y-m-d', strtotime($date));
            $day = date('D', strtotime($date));
            $date_by_day[$day][] = $date;
        }
        
        return $date_by_day;
    }
```

## output
```
array:7 [▼
  "Mon" => array:5 [▼
    0 => "2021-03-01"
    1 => "2021-03-08"
    2 => "2021-03-15"
    3 => "2021-03-22"
    4 => "2021-03-29"
  ]
  "Tue" => array:5 [▼
    0 => "2021-03-02"
    1 => "2021-03-09"
    2 => "2021-03-16"
    3 => "2021-03-23"
    4 => "2021-03-30"
  ]
  "Wed" => array:5 [▼
    0 => "2021-03-03"
    1 => "2021-03-10"
    2 => "2021-03-17"
    3 => "2021-03-24"
    4 => "2021-03-31"
  ]
  "Thu" => array:4 [▶]
  "Fri" => array:4 [▶]
  "Sat" => array:4 [▶]
  "Sun" => array:4 [▶]
]
```
