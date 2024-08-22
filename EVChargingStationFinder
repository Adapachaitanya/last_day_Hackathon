import java.util.*;

class ChargingStation {
    String name;
    String location;
    int availableSlots;

    ChargingStation(String name, String location, int availableSlots) {
        this.name = name;
        this.location = location;
        this.availableSlots = availableSlots;
    }

    public void bookSlot() {
        if (availableSlots > 0) {
            availableSlots--;
            System.out.println("Slot booked successfully at " + name + ", " + location);
        } else {
            System.out.println("No slots available at " + name + ", " + location);
        }
    }

    @Override
    public String toString() {
        return "Name: " + name + ", Location: " + location + ", Available Slots: " + availableSlots;
    }
}

public class EVChargingStationFinder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        List<ChargingStation> stations = new ArrayList<>();
        stations.add(new ChargingStation("Station A", "Mukteswaram", 5));
        stations.add(new ChargingStation("Station B", "veeravallipalem", 2));
        stations.add(new ChargingStation("Station C", "Ainavalli", 0));

        while (true) {
            System.out.println("\nAvailable Charging Stations:");
            for (int i = 0; i < stations.size(); i++) {
                System.out.println((i + 1) + ". " + stations.get(i));
            }

            System.out.println("\nEnter the number of the station to book a slot (0 to exit):");
            int choice = scanner.nextInt();

            if (choice == 0) {
                break;
            } else if (choice > 0 && choice <= stations.size()) {
                stations.get(choice - 1).bookSlot();
            } else {
                System.out.println("Invalid choice. Please try again.");
            }
        }

        scanner.close();
    }
}
