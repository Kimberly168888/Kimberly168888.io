package application;
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.control.ListView;
import javafx.scene.control.ScrollPane;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.HBox;
import javafx.scene.layout.StackPane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Rectangle;
import javafx.stage.Stage;
import javafx.collections.FXCollections;

public class Main extends Application {

    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) {
        primaryStage.setTitle("Programa uwu");

        BorderPane root = new BorderPane();

        ListView<StackPane> leftListView = new ListView<>();
        leftListView.setItems(FXCollections.observableArrayList(
                createLabeledBox("  KIMBERLY VINCES", new Image("https://th.bing.com/th/id/R.c82c1db95bb3145f4af08a8834a1a5b8?rik=HI1a02hh9LjZvA&riu=http%3a%2f%2fimages6.fanpop.com%2fimage%2fphotos%2f39500000%2fjustin-bieber-purpose-world-tour-2016-justin-bieber-39519483-2500-2500.jpg&ehk=Pv9RqOQkbqAbUO%2fyslLfPfUaIvCFAl69gLSnKzYo4Hs%3d&risl=&pid=ImgRaw&r=0")),
                createLabeledBox("  ERIKA VINCES", new Image("https://cdn01.justjared.com/wp-content/uploads/headlines/2016/12/justin-bieber-announces-six-dates-for-2017-stadium-tour.jpg")),
                createLabeledBox("  MARIA JOSE VINCES", new Image("https://www.needsomefun.net/wp-content/uploads/2020/05/justin-bieber-stage.jpg")),
                createLabeledBox("  ALEJANDRA VINCES", new Image("https://th.bing.com/th/id/R.70e65fb64666233fe7909528cc5be373?rik=HYVCvTOdHRXEHg&riu=http%3a%2f%2fgetwallpapers.com%2fwallpaper%2ffull%2f4%2f5%2f9%2f927274-justin-bieber-purpose-wallpapers-1920x1080-for-computer.jpg&ehk=cfibieFgenW4%2biR5kxJMdlbFwDKqXIlb6pgmrWzvY5M%3d&risl=&pid=ImgRaw&r=0")),
                createLabeledBox("  JOSE VINCES", new Image("https://cleepr.ru/images/justin-bieber-purpose/14.jpg"))
        ));
        leftListView.setPrefSize(200, 300);

        ScrollPane leftScrollPane = new ScrollPane(leftListView);
        leftScrollPane.setFitToWidth(true);
        leftScrollPane.setVbarPolicy(ScrollPane.ScrollBarPolicy.ALWAYS);
        leftScrollPane.setHbarPolicy(ScrollPane.ScrollBarPolicy.NEVER);

        // Crear un rectángulo negro
        Rectangle blackRectangle = new Rectangle(200, 400);
        blackRectangle.setFill(Color.BLACK);

        // Aplicar el rectángulo negro en un StackPane
        StackPane blackStackPane = new StackPane(blackRectangle);

        // Aplicar el ListView y el StackPane negro en un HBox
        HBox hbox = new HBox(leftScrollPane, blackStackPane);

        root.setCenter(hbox);

        Scene scene = new Scene(root, 500, 300);
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    private StackPane createLabeledBox(String labelText, Image image) {
        Label label = new Label(labelText);

        ImageView imageView = new ImageView(image);
        imageView.setFitWidth(20);
        imageView.setFitHeight(20);

        
        HBox hBox = new HBox();
        hBox.getChildren().addAll(imageView, label);

        StackPane stackPane = new StackPane();
        stackPane.getChildren().add(hBox);
        return stackPane;
    }
}



![image](https://github.com/Kimberly168888/Kimberly168888.io/assets/169225018/b75c8c0e-6738-4321-832d-1fa073e55be2)



