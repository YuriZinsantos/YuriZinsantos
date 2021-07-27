import 'package:flutter/material.dart';



class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(

      ),
      body: ListView(
        children: [
          Image.asset(
            'images/hotdogguri.png',
            fit: BoxFit.cover,
          ),
          Image.asset(
            'images/cardapiodosguri.png',
            fit: BoxFit.fill,
          ),
          Padding(padding: EdgeInsets.all(32)),
          Center(
            child: ElevatedButton.icon(
              onPressed: () {
                Navigator.push(
                    context,
                    //direcionando para outra página
                    MaterialPageRoute(builder: (context) => hotdogs()));
              },
              icon: Icon(Icons.arrow_right),

            ),
          ),
        ],
      ),
    );
  }
}

class hotdogs extends StatefulWidget {
  const hotdogs({Key? key}) : super(key: key);

  @override
  _hotdogsState createState() => _hotdogsState();
}

class _hotdogsState extends State<hotdogs> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("cardapio"),
      ),
      body: ListView(
          children: [
      ListTile(
      leading: Icon(Icons.contacts),
      title: Text('Bebidas'),
      onTap: () {
        Navigator.push(
            context,
            MaterialPageRoute(builder: (context)=>MyFavoritehotdog()));
      },
    ),
    ListTile(
    leading: Icon(Icons.person),
    title: Text("Xis"),
    ),
    ListTile(
    leading: Icon(Icons.settings),
    title: Text("Cachorrao"),
    ),
    ListTile(
    leading: Icon(Icons.picture_in_picture_rounded),
    title: Text("Images Bebidas"),
    ),
    ElevatedButton(
    onPressed: (){},
    child: Text("Pesquisar cardapio"),
    ),
    Image.asset(
    'images/hotdogguri.png',
    fit: BoxFit.cover,
    ),
    Image.asset(
    'images/hotdogguri.png',
    ),
    );

    );

  }

}
class MyFavoritehotdog extends StatefulWidget {
  const MyFavoritehotdog({Key? key}) : super(key: key);

  @override
  _MyFavoritehotdogState createState() => _MyFavoritehotdogState();
}

class _MyFavoritehotdogState extends State<MyFavoritehotdog> {
  @override
  Widget build(BuildContext context) {
    return Scaffold (
      appBar: AppBar(
        title: Text('pedidos'),
      ),
      body: ListView(
          children: [
      ListTile(
      leading: Icon(Icons.workspaces),
      title: Text('Bebidas'),
      ),
    )

    ),

    );
    ),
    ],
  }

