# The functional requirements of EcoGrid Energy system are:

1. Marketplace service creates trade request.
2. Settlement Service reserves customer funds.
3. Allocate enough energy using SmartMeter service.
4. Send notifications to the users.

# Python Code:
class MarketplaceService:

    def create_trade(self):
        print("Trade Status: Pending")

    def confirm_trade(self):
        print("Trade Status: Confirmed")

    def cancel_trade(self):
        print("Trade Status: Cancelled")


class SettlementService:

    def reserve_funds(self):
        print("Funds Reserved")

    def release_funds(self):
        print("Funds Released")


class SmartMeterService:

    def allocate_energy(self):

        energy_available = False

        if energy_available:
            print("Energy Allocated")

        else:
            raise Exception("Energy Allocation Failed")


# Create Services
marketplace = MarketplaceService()

settlement = SettlementService()

meter = SmartMeterService()


try:

    # Step 1
    marketplace.create_trade()

    # Step 2
    settlement.reserve_funds()

    # Step 3
    meter.allocate_energy()

    # Step 4
    marketplace.confirm_trade()

except:

    print("Compensation Transaction Started")

    settlement.release_funds()

    marketplace.cancel_trade()
    

  # Ouput 

  ![Output](EcoGrid.png)
    
