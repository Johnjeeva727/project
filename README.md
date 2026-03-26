import jakarta.persistence.*;
import java.math.BigDecimal;

@Entity
public class BankAccount {

    @Id
    private String accountNumber;

    private String accountHolderName;

    @Column(precision = 19, scale = 4)
    private BigDecimal balance;

    @Embedded
    private Currency currency;

    // getters and setters
}
