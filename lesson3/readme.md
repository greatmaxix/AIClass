# hw3

## Class task
```
class BasePlayer {
    pass() {
        pass ball to open teammate
    }

    doBaseActions(state)
    { 
        if (state.canKick()) {
            pass()
        }
    }
}

class freeKickTaker() extends BasePlayer {
    tryAction(state) {
        if (state.freeKick())
            doFreeKick()
        doBaseActions(state)
    }

    doFreeKick() {
        pass or try to score
    }
}


class Attacker () extends BasePlayer {
    tryAction(state) {
        if (state.canGetBall())
            getBall()
        if (state.canKick())
            kick()
        doBaseActions(state)
    }

    getBall() {
        try to get ball
    }

    scoreGoal() {
        try to score
    }
}

class Defender () extends BasePlayer {
    tryAction(state) {
        if (state.canBlock())
            block()
        if (state.mark())
            mark()
        doBaseActions(state)
    }

    block() {
        try to block
    }

    mark() {
        try to mark
    }
}

class Player () extends BasePlayer {
    tryAction(state) {
        if (state.canGoZone())
            goZone()
        doBaseActions(state)
    }

    goZone() {
        go to the zone
    }
}

for aech pair:
    initState()
    while eval is not finished:
        for each player on both team:
            player.tryAction(state)
            updateState()
        eval = computeFitness()

```