## Ambulance task

class AmbulanceTeam {
    setBuilding(building) {

    }

    doAction () {
        exploreBuildings()
    }

    exploreBuildings() {
        collectCivsWithPriority()
    }
}

class FireBrigades {
    assignRegion (region)

    assignBuildingToBeSaved(buildin)

    doAction () {
        checkForFire()
    }
}

class FireCenter {
    doAction () {
        assignRegionsForBrigades()
        startAuction()
    }

    startAuction () {
        # some logic and loop builing assignment to a brigade
    }
}

class Center {
    addCivs(civ) {
        allCivs.push(civ)
    }

    doAction () {
        assingTeams()
        startAuction()
    }

    assignTeams() {
        for each ambulanceTeam as team:
            team.setBuilding(building)
    }

    startAuction () {
        if time != 2
            return

        # loops through teams, calculates and stores exploreBuildings in priority list

        if (!owner.accepted(civ)) {
            reopenAuction
        }
    }
}

