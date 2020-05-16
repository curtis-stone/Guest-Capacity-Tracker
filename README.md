# Guest-Capacity-Tracker
JavaScript functions that allows you to keep track of capacity/capacity limits of a workplace

    // restaurant guest tracker 
    let restaurant = {
        name: `Stone Grill`,
        guestCapacity: 75,
        guestCount: 0}

        // Check seat availability based on capacity of restaurant and current guest count
        // returns a boolean that determines if there is enough space for the guest(s)
        function checkAvailability(partySize) {
           let seatsLeft = restaurant.guestCapacity - restaurant.guestCount
           return partySize <= seatsLeft
        } 

        // adds to the current amount of seated guests
        function seatParty(partySize) {
            restaurant.guestCount = restaurant.guestCount + partySize
        }

        // removes guests from the total amount of seated guests
        function removeParty(partySize) {
            restaurant.guestCount = restaurant.guestCount - partySize
        }

    seatParty(72) //sets guest count 72/75 of the max capacity
    console.log(checkAvailability(4)) //checks if 4 guests can be seated (returns false (76/75))
    removeParty(5) //removes 5 guests from the total amount currently seated (71/75)
    console.log(checkAvailability(4)) // cecks if 4 guests can be seated, returns true (75/75)
