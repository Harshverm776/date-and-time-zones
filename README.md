# Date & Time Zones  

In this article, I am going to cover the basics of date and time zones which is required if you are working on Dates. Also, As a programmer you must know this thing.  

## Topics to be covered-  

1. Standard Definition  
   GMT  
   UTC  
   ISO  
   Local  
   Daylight saving time  

2. In Simple Words
3. Note
4. Program

## 1. Standard Definiton

### GMT (Greenwich Mean Time)-  

>GMT is the time displayed by the Shepherd Gate Clock at the Royal Observatory in Greenwich, London. When the sun is at its highest point exactly above the Prime Meridian, it is 12:00 noon at Greenwich.  

### UTC (Coordinated Universal Time)-  

>UTC is the primary time standard by which the world regulates clocks and time. It is within about 1 second of mean solar time at 0° longitude and is not adjusted for daylight saving time. It is effectively a successor to Greenwich Mean Time (GMT).  

### ISO (International Organization for Standardization)-  

>ISO 8601 is an international standard covering the worldwide exchange and communication of date- and time-related data. It is maintained by the Geneva-based International Organization for Standardization (ISO) and was first published in 1988, with updates in 1991, 2000, 2004, and 2019.  

### Local-  

>Local time is the time observed in a specific locality. There is no canonical definition. Originally it was mean solar time, but since the introduction of time zones it is generally the time as determined by the time zone in effect, with daylight saving time where and when applicable.  

### Daylight saving time-  

>Daylight saving time (DST) is the practice of setting the clocks forward one hour from standard time during the summer months and back again in the fall, in order to make better use of natural daylight.  

## 2. In Simple Words

* **GMT-**  
  GMT is the old standard which was used earlier. It is determined by the location of sun. But now, It got replaced with UTC which determine time more precisely.  

  Also, It is the solar time at 0 degree longitude i.e., Prime Meridian.  

![Prime Meridian](https://cdn.britannica.com/63/2063-050-89E52B49/Perspective-globe-grid-parallels-meridians-longitude-latitude.jpg)  

* **UTC-**  
UTC is the standard which is used world wide for the determination of time.  
***Like-*** ` UTC + 05:30 `  

* **Time Zones-**  
Earth is divided into different zones which uses same local time/ standard time.  

![Time Zones](https://laulima.hawaii.edu/access/content/group/dbd544e4-dcdd-4631-b8ad-3304985e1be2/book/chapter_1/timzone.gif)

* **ISO-**
It is International standard i.e., format used world wide. Also called ISO 8601 standard.  
***Like-*** ` 2021-12-16T13:55:18.477Z `  

* **Local-**  
The time where you live.  

* **Daylight saving time-**  
It is used at many places in the world for better use of daylight.  
It is the practice of setting the clocks forward one hour from standard time during the summer months, and back again in the fall, in order to make better use of natural daylight.

## 3. Note

* UTC and GMT are almost same. Don't get confuse between them.  
* Always use ISO instead of UTC because ISO also specify millisecond as well.  

* **Types of time-**  
  1. **Local**  
  2. **UTC/GMT**  
  3. **ISO**

## 4. Program  

### JavaScript code-  

```js


const date = new Date()

console.log(date)
console.log("date- " + date)

console.log("toString- " + date.toString())
console.log("toDateString- " + date.toDateString())

console.log("toLocaleString- " + date.toLocaleString())
console.log("toUTCString- " + date.toUTCString())
console.log("toISOString- " + date.toISOString())

console.log("getTimezoneOffset- " + date.getTimezoneOffset())

console.log("TimeZone- " + Intl.DateTimeFormat().resolvedOptions().timeZone)

```  

| Console            | Output                                                  |
| ------------------ | ------------------------------------------------------- |
|                    | 2021-12-17T05:37:30.827Z                                |
| date-              | Fri Dec 17 2021 11:07:30 GMT+0530 (India Standard Time) |
| toString-          | Fri Dec 17 2021 11:07:30 GMT+0530 (India Standard Time) |
| toDateString-      | Fri Dec 17 2021                                         |
| toLocaleString-    | 12/17/2021, 11:07:30 AM                                 |
| toUTCString-       | Fri, 17 Dec 2021 05:37:30 GMT                           |
| toISOString-       | 2021-12-17T05:37:30.827Z                                |
| getTimezoneOffset- | -330                                                    |
| TimeZone-          | Asia/Calcutta                                           |  

---
---

#### Sources  

* Videos-  
  * [GMT, Time Zones & Indian Standard Time](https://youtu.be/viyERCiHgj0)  
* Websites-  
  * [Time Zones for Software Developers](https://betterprogramming.pub/time-zones-for-software-developers-7f21d5a407aa)  
  * [UTC vs ISO format for time](https://stackoverflow.com/questions/58847869/utc-vs-iso-format-for-time)  
