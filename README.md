
<!-- Full Shade/Part Shade/Part Sun/Full Sun -->
Sun = 0 --> 4

rec_plant_data = TREFLE DATA
plant_data = USER

USER:
|___ HOME (many)
    |_ Indoor 
      |_ Room (Where is the plant exactly.) V2!
         |_ Plants (The thing we are tracking) 
           |_

    |_ Outdoor
     |_ Location (Where is the plant exactly) V2!
       |_ Plants


class Plant:
  required_sun = Int() # 0 (All shade) --> 4 (All sun)
  actual_sun = Int() # 0 (All shade) --> 4 (All sun)
  
  hardiness_zone = Int()  
  water_schedule =  

  def get_current_plant_status(self):
    if self.home.season() === 'WINTER':
    <!-- Change feeding schedule -->


  def show_stats(self):
    
    get_current_plant_status()

    return self.plant_fields


  # v2:
  health_checklist = JSON_Field():
    - Is the soil dry?
    - Last time you fed?
    - Signs/symptoms of insects or disease?



  HP = 100 
  |_ Outdoor 



V1 Goals:

Setup models / db for the above.

1) Add a User (Login/Sign up page) --> Simple form for now - can build out auth later.
2) Add a Home and rooms.

3) Add plants.  
|___ Take a picture (support imgs in DB)
|___ 



ADD a HOME:

Inputs:
  (Temperature should be a one-time thing.  No need to check it every time)
  - Location (to define the hardiness level) - user defined? (whats the minimum temp in your house)?
  |___ Maybe ping a weather service? If so, we need an address.

Notes:
  - Use hardiness zone for plant suggestion
  - Track seasons (4 dif seasons)
  |___ Plants will rely on this.


ADD A PLANT: 
(Greg finish this)


UX:
First time flow

Login/Sign up --> Add Home --> Add Plants

(The primary view)
Dashboard view:
- See a list of plants. (how should this be ordered?)
- Clicking a plant shows the overview of the plant (for home).
- Clicking the plant in the overview shows the facts about the plant (API data).

TODO:

- What does plant overview look like? 
- How does search look and work?
- Plant stats page (trefle data) - what do we show??


- How do mark a plant as 'tended to'/'done'.  If someone handles it earlier than notification.
- Does the notification 


PLANT X NEEDS TO BE WATERD (click this)  ----> Plant X Overview Page --> Press the water btn.

Home (Watered all)  --> Marks all plants as complete....