# $$x^2$$ First Chapter

GitBook allows you to organize your book into chapters, each chapter is stored in a separate file like this one.

You can do Math!  $$\ln\left(1+\frac{x}{1+x}\right)$$

HEre's a table

| x | y |
| :--- | :--- |
| 0 | 1 |
| 1 | 2 |
| 2 | 4 |
| 3 | 8 |
| 4 | 16 |

```java
import etomica.*

/**
 * Here is my simulation
 */

Simulation mySimulation = new Simulation();

real x = 5.3;
x++;
real y = Math.sin(x);

//AEE 
MeterMappedAveraging AEEMeter = null;
AccumulatorAverageCovariance AEEAccumulator = null;
if(aEE){
    AEEMeter = new MeterMappedAveraging(sim.space, sim.box, sim,temperature,interactionS,dipoleMagnitude,sim.potentialMaster);
    AEEAccumulator = new AccumulatorAverageCovariance(samplePerBlock,true);
    DataPump AEEPump = new DataPump(AEEMeter,AEEAccumulator);
    IntegratorListenerAction AEEListener = new IntegratorListenerAction(AEEPump);
    AEEListener.setInterval(sampleAtInterval);
    sim.integrator.getEventManager().addListener(AEEListener);
}
```



