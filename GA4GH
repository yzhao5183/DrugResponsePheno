package edu.archive;

import org.json.simple.JSONArray;
import org.json.simple.JSONObject;
import org.json.simple.parser.JSONParser;
import org.json.simple.parser.ParseException;
import org.jsoup.Jsoup;
import org.jsoup.nodes.Document;
import org.jsoup.select.Elements;
import org.xml.sax.SAXException;
import org.w3c.dom.Node;
import org.w3c.dom.Element;

import javax.xml.parsers.*;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.FileReader;
import java.io.IOException;
import java.io.PrintWriter;
import java.io.UnsupportedEncodingException;
import java.lang.reflect.Array;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Date;
import java.util.HashMap;
import java.util.HashSet;
import java.util.List;
import java.util.Map;
import java.util.Set;
import java.util.concurrent.TimeUnit;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class GA4GH {
	
	public static String[] groups = {};
	public static ArrayList<String> out = new ArrayList<>();
	public static HashMap<String,String> id = new HashMap<String,String>();
	public static String[] chemicals = {"2-amino-1-phenylethanol derivatives","2-methoxyestradiol","3,4-methylenedioxymethamphetamine","3,5-dimethyl-2-(3-pyridyl)thiazolidin-4-one","3-aminopyridine-2-carboxaldehyde thiosemicarbazone","3-beta-hydroxy-5-androsten-17-one","3-cyano-7-ethoxycoumarin","3-oxoandrosten (4) derivatives","4,6,4'-trimethylangelicin","4-methylthioamphetamine","4-methylumbelliferone","5-androstanon (3) derivatives","6,7-dihydroxybergamottin","6-o-phosphoryl inosine monophosphate","8-cyclopentyl-1,3-dipropylxanthine","abacavir","abarelix","abatacept","abciximab","abemaciclib","abiraterone","ABT-751","acamprosate","acarbose","acebutolol","aceclofenac","ACE inhibitors and calcium channel blockers","ACE inhibitors and diuretics","Ace Inhibitors, Combinations","Ace Inhibitors, Plain","acemetacin","acenocoumarol","acepromazine","aceprometazine","acetamide mea","acetaminophen","acetaminophen / codeine","acetaminophen/propoxyphene napsylate","acetaminophen / tramadol","acetanilide","acetazolamide","acetic acid","Acetic acid derivatives and related substances","acetohexamide","acetohydroxamic acid","acetone","acetophenazine","acetylcholine","acetylcysteine","acetyldigitoxin","aciclovir","Acidifiers","Acid preparations","acitretin","Acridine derivatives","Acth","Actinomycines","adalimumab","Adamantane derivatives","adapalene","adefovir dipivoxil","adenine","adenosine","adenosine diphosphate","adenosine monophosphate","adenosine triphosphate","adinazolam","Adrenergic and dopaminergic agents","Adrenergics and other drugs for obstructive airway diseases","Adrenergics For Systemic Use","adrenergics, inhalants","afatinib","afatinib dimaleate","aflatoxin b1","aflibercept","afutuzumab","agalsidase beta","Agents Acting On The Renin-angiotensin System","Agents Against Amoebiasis And Other Protozoal Diseases","Agents Against Leishmaniasis And Trypanosomiasis","Agents For Treatment Of Hemorrhoids And","agomelatine","ajmaline","albendazole","alcaftadine","alclometasone","Aldehydes and derivatives","aldesleukin","Aldose reductase inhibitors","Aldosterone antagonists","alectinib","alefacept","alemtuzumab","alendronate","alfacalcidol","alfentanil","alfuzosin","alglucerase","alglucosidase alfa","Alimentary Tract And Metabolism","alirocumab","alisertib","aliskiren","alitretinoin","alizapride","Alkaloids, excl. rauwolfia","Alkaloids, excl. rauwolfia, in combination with diuretics","Alkylating Agents","Alkyl sulfonates","Allergen extracts","Allergens","allopregnanolone","allopurinol","All Other Non-therapeutic Products","All Other Therapeutic Products","allylestrenol","almitrine","almokalant","almotriptan","aloe","alosetron","alox5-pathway modifiers","alpelisib","alpha-1-proteinase inhibitor","Alpha-adrenoreceptor antagonists","Alpha-adrenoreceptor antagonists and diuretics","Alpha- and beta-adrenoreceptor agonists","Alpha and beta blocking agents","Alpha and beta blocking agents and other diuretics","Alpha and beta blocking agents and thiazides","Alpha glucosidase inhibitors","alpha-linolenic acid","alpha-methyl-para-tyrosine","alprazolam","alprenolol","alprostadil","alseroxylon","alteplase","altretamine","aluminium","Aluminium agents","Aluminium compounds","aluminum chloride","aluminum hydroxide","alverine","alvespimycin","alvimopan","amantadine","ambenonium","ambrisentan","amcinonide","amdinocillin","amfenac","Amides","amifampridine","amifampridine phosphate","amifostine","amikacin","amiloride","amino acids","Amino acids and derivatives","Amino acids/carbohydrates/minerals/vitamins, combinations","Amino acids, incl. combinations with polypeptides","Aminoalkyl ethers","aminobenzoic acid","aminocaproic acid","aminoglutethimide","aminoglycoside antibacterials","aminohippurate","aminolevulinic acid","aminophenazone","aminophylline","aminopterin","Aminoquinolines","aminosalicylic acid","Aminosalicylic acid and derivatives","Aminosalicylic acid and similar agents","amiodarone","amisulpride","amitriptyline","amlexanox","amlodipine","amlodipine / atorvastatin / perindopril arginine","ammonia","ammonium chloride","ammonium lactate","amobarbital","amodiaquine","amoxapine","amoxicillin","Amphenicols","amphetamine","amphotericin b","ampicillin","amprenavir","amrinone","amsacrine","amyl nitrite","Anabolic Agents For Systemic Use","Anabolic Steroids","anacetrapib","anagrelide","anakinra","Analgesics","Analgesics and anesthetics","anastrozole","Androgen, progestogen and estrogen in combination","androgens and estrogens","Androgens And Female Sex Hormones In Combination","Androgens and female sex hormones in combination with other drugs","androgens for topical use","Androstan derivatives","Angiotensin II Antagonists","Angiotensin II antagonists and calcium channel blockers","Angiotensin II antagonists and diuretics","Angiotensin II Antagonists, Combinations","anidulafungin","anileridine","Anilides","anisindione","anisotropine methylbromide","anistreplase","antacids","Antacids, other combinations","Antacids with antiflatulents","Antacids with antispasmodics","Antacids with sodium bicarbonate","antazoline","Anterior Pituitary Lobe Hormones And Analogues","Anthelmintics","anthracyclines and related substances","Anthrax vaccines","Anti-acne Preparations","Anti-acne Preparations For Systemic Use","Anti-acne Preparations For Topical Use","Antiadrenal Preparations","Antiadrenergic Agents, Centrally Acting","Antiadrenergic Agents, Ganglion-blocking","Antiadrenergic Agents, Peripherally Acting","Antiallergic agents, excl. corticosteroids","Antiandrogens","Anti-androgens","Antiandrogens and estrogens","Antiandrogens, plain","Antianemic Preparations","Antiarrhythmics, class Ia","antiarrhythmics, class i and iii","Antiarrhythmics, class Ib","Antiarrhythmics, class Ic","Antiarrhythmics, class III","Antibacterials For Systemic Use","Antibiotics","Antibiotics And Chemotherapeutics, Combinations","Antibiotics And Chemotherapeutics For Dermatological Use","Antibiotics and corticosteroids","Antibiotics For Topical Use","Anticestodals","Anticholinergic Agents","Anticholinergics","Anticholinesterases","Anticorticosteroids","Anti-dementia Drugs","antidepressants","Antidepressants in combination with psycholeptics","Antidiarrheal Microorganisms","Antidiarrheals, Intestinal Antiinflammatory/antiinfective","Antidotes","Antiemetics And Antinauseants","antiepileptics","Anti-estrogens","Antifibrinolytics","Antifungals For Dermatological Use","Antifungals For Systemic Use","Antifungals For Topical Use","antiglaucoma preparations and miotics","Anti-gonadotropin-releasing hormones","Antigonadotropins and similar agents","Antigout Preparations","Antigrowth hormones","antihemophilic factor","Antihemorrhagics","Antihidrotics","Antihistamines For Systemic Use","Antihypertensives","Antihypertensives And Diuretics In Combination","Antiinfectives","Antiinfectives And Antiseptics, Excl. Combinations","Antiinfectives and antiseptics for local oral treatment","Antiinfectives/antiseptics In Combination With Corticosteroids","Antiinfectives For Systemic Use","Antiinfectives for treatment of acne","Antiinflammatory Agents","Antiinflammatory Agents And Antiinfectives In Combination","Antiinflammatory agents, non-steroids","Antiinflammatory agents, non-steroids and antiinfectives in combination","Antiinflammatory And Antirheumatic Products","antiinflammatory and antirheumatic products, non-steroids","Antiinflammatory/antirheumatic Agents In Combination","Antiinflammatory/antirheumatic agents in combination with corticosteroids","Antiinflammatory preparations, non-steroids for topical use","Antiinflammatory products for vaginal administration","Antimalarials","antimetabolites","Antimigraine Preparations","Antimony compounds","antimony potassium tartrate","Antimycobacterials","Antimycotics For Systemic Use","Antinematodal Agents","antineoplastic agents","Antineoplastic And Immunomodulating Agents","Antineovascularisation agents","Antiobesity Preparations, Excl. Diet Products","Antiparasitic Products, Insecticides And Repellents","Anti-parathyroid Agents","Anti-parkinson Drugs","Antiprogestogens","Antipropulsives","Antiprotozoals","Antipruritics, Incl. Antihistamines, Anesthetics, Etc.","Antipsoriatics","Antipsoriatics For Systemic Use","Antipsoriatics For Topical Use","antipsychotics","antipyrine","Antiseptics","Antiseptics and corticosteroids","Antiseptics And Disinfectants","Antispasmodics And Anticholinergics In Combination With Other Drugs","Antispasmodics In Combination With Analgesics","Antispasmodics in combination with other drugs","Antispasmodics In Combination With Psycholeptics","Antispasmodics, psycholeptics and analgesics in combination","antithrombotic agents","antithymocyte globulin","Antithyroid Preparations","Antitrematodals","Antivaricose Therapy","Antivertigo Preparations","antivirals","Antivirals For Systemic Use","Antivirals for treatment of HIV infections, combinations","Antracen derivatives","antrafenine","Anxiolytics","apixaban","apomorphine","Appetite Stimulants","apple juice","apraclonidine","aprepitant","aprindine","aprobarbital","aprotinin","arbekacin","arbutamine","arcitumomab","ardeparin","arformoterol","argatroban","aripiprazole","aripiprazole lauroxil","Arsenic compounds","arsenic trioxide","arsenite","arteether","artemether","artemisinin","artemisinin and derivatives","Arteriolar Smooth Muscle, Agents Acting On","artesunate","articaine","articaine / epinephrine","arylhydrazines","Aryloxyacetic acid derivatives","Ascorbic acid (vitamin C), combinations","Ascorbic Acid (vitamin C), Incl. Combinations","Ascorbic acid (vitamin C), plain","asparaginase","aspartame","aspirin","astemizole","asunaprevir","ataluren","atazanavir","atazanavir / cobicistat","atazanavir / ritonavir","atenolol","atezolizumab","atomoxetine","atorvastatin","atovaquone","atracurium","atrasentan","atropine","attapulgite","auranofin","avanafil","avatrombopag","avelumab","Avermectines","axitinib","azacitidine","azapropazone","Azaspirodecanedione derivatives","azatadine","azathioprine","AZD1152","azelaic acid","azelastine","azidocillin","azithromycin","azlocillin","aztreonam","bacampicillin","bacitracin","baclofen","Bacterial And Viral Vaccines, Combined","Bacterial Vaccines","balsalazide","bambuterol","Bamocaftor","barbital","Barbiturates, combinations","Barbiturates in combination with other drugs","barbiturates, plain","barium sulfate","Barium sulfate containing X-ray contrast media","basiliximab","becaplermin","beclomethasone","bedaquiline","belimumab","belinostat","Belladonna alkaloids, semisynthetic, quaternary ammonium compounds","Belladonna alkaloids, tertiary amines","Belladonna and derivatives in combination with analgesics","Belladonna and derivatives in combination with psycholeptics","Belladonna And Derivatives, Plain","benazepril","bendroflumethiazide","benoxaprofen","Benserazide","bentiromide","bentoquatam","benzaldehyde","Benzamides","benzbromarone","benzene","Benzimidazole derivatives","benzocaine","benzodiazepine derivatives","Benzodiazepine related drugs","benzoic acid","Benzomorphan derivatives","benzonatate","Benzothiazepine derivatives","benzoyl peroxide","benzphetamine","benzquinamide","benzthiazide","benztropine","benzydamine","benzyl alcohol","benzyl benzoate","benzylpenicilloyl polylysine","bepotastine","bepridil","berberine","beryllium","Beta Blocking Agents","Beta Blocking Agents And Other Antihypertensives","Beta Blocking Agents And Other Diuretics","Beta Blocking Agents And Thiazides","Beta Blocking Agents And Vasodilators","Beta blocking agents, non-selective","Beta blocking agents, non-selective, and other antihypertensives","Beta blocking agents, non-selective, and other diuretics","Beta blocking agents, non-selective, and thiazides","Beta blocking agents, non-selective, and vasodilators","Beta blocking agents, non-selective, thiazides and other diuretics","Beta blocking agents, selective","Beta blocking agents, selective, and other antihypertensives","Beta blocking agents, selective, and other diuretics","Beta blocking agents, selective, and thiazides","Beta blocking agents, selective, and vasodilators","Beta blocking agents, selective, thiazides and other diuretics","Beta Blocking Agents, Thiazides And Other Diuretics","beta carotene","betahistine","betaine","beta-lactam antibacterials, penicillins","Beta-lactamase inhibitors","Beta-lactamase resistant penicillins","Beta-lactamase sensitive penicillins","betamethasone","betaxolol","betazole","bethanechol","bethanidine","bevacizumab","bevantolol","bexarotene","bezafibrate","bicalutamide","bifonazole","Biguanides","Biguanides and amidines","bile acid preparations","Bile And Liver Therapy","bilirubin","bimatoprost","binimetinib","Bioflavonoids","biotin","biperiden","Biricodar","bisantrene","Bismuth preparations","bismuth subsalicylate","bisoprolol","bisoprolol fumarate / perindopril arginine","Bisphosphonates","Bisphosphonates, combinations","Bisquaternary ammonium compounds","bivalirudin","bleomycin","blinatumomab","Blood And Blood Forming Organs","Blood And Related Products","Blood coagulation factors","Blood Glucose Lowering Drugs, Excl. Insulins","Blood Substitutes And Perfusion Solutions","Blood substitutes and plasma protein fractions","Blood tests, auxiliary products","Blood transfusion, auxiliary products","bnp-32","boceprevir","Bone morphogenetic proteins","bopindolol","Boric acid products","bortezomib","bosentan","bosutinib","botulinum toxin type a","botulinum toxin type b","brentuximab vedotin","bretylium","brexpiprazole","brigatinib","brimonidine","brinzolamide","brivanib","brivaracetam","brivudine","bromazepam","bromfenac","bromocriptine","bromodiphenhydramine","bromperidol","brompheniramine","brostallicin","brotizolam","Brucellosis vaccines","BSI-201","bucillamine","bucindolol","buclizine","budesonide","bufuralol","Bulk producers","bumetanide","bupivacaine","bupranolol","buprenorphine","buprenorphine / naloxone","bupropion","buserelin","buspirone","busulfan","butabarbital","butalbital","butenafine","butethal","butoconazole","butorphanol","butylated hydroxytoluene","Butylpyrazolidines","Butyrophenone derivatives","cabazitaxel","cabergoline","cabozantinib","caffeine","calcein","calcidiol","Calcineurin inhibitors","calcipotriol","Calcitonin preparations","calcitriol","calcium","calcium acetate","calcium carbonate","calcium channel blockers","Calcium Channel Blockers And Diuretics","calcium chloride","Calcium, combinations with other drugs","Calcium compounds","calcium gluceptate","calcium gluconate","Calcium Homeostasis","calcium pantothenate","calcium phosphate","camptothecin","canakinumab","candesartan","candesartan cilexetil","candicidin","candoxatril","canertinib","cangrelor","cannabidiol","cannabinoids","capecitabine","Capillary Stabilizing Agents","capreomycin","capromab","capsaicin","Capsaicin and similar agents","captopril","carbachol","Carbamates","carbamazepine","Carbamic acid esters","Carbamide products","Carbapenems","carbasalate calcium","carbenicillin","carbetocin","carbidopa","carbimazole","carbinoxamine","carbocisteine","carbohydrates","Carbohydrates/proteins/minerals/vitamins, combinations","carbon dioxide","carbonic anhydrase inhibitors","carboplatin","carboprost tromethamine","Carboxamide derivatives","Cardiac Glycosides","Cardiac Stimulants Excl. Cardiac Glycosides","Cardiac Therapy","Cardiovascular System","carfilzomib","carglumic acid","Caries prophylactic agents","cariprazine","carisoprodol","carmustine","carphenazine","carprofen","carrageenan","carteolol","carvedilol","casopitant","caspofungin","castor oil","catecholamines","cationic xenobiotics","cavosonstat","CBLB502","cefacetrile","cefaclor","cefadroxil","cefalotin","cefamandole","cefazolin","cefdinir","cefditoren","cefepime","cefixime","cefmenoxime","cefmetazole","cefonicid","cefoperazone","ceforanide","cefotaxime","cefotetan","cefotiam","cefoxitin","cefpiramide","cefpodoxime","cefprozil","cefradine","ceftazidime","ceftibuten","ceftizoxime","ceftriaxone","cefuroxime","celecoxib","Celiprolol","cellulose","Centrally acting antiobesity products","Centrally acting sympathomimetics","cephalexin","cephaloglycin","cephapirin","ceritinib","cerivastatin","cerliponase alfa","certolizumab pegol","cerulenin","ceruletide","cetirizine","cetrorelix","cetuximab","cevimeline","charcoal preparations","Chemicals and reagents for analysis","Chemotherapeutics For Topical Use","chenodeoxycholic acid","chlophedianol","chloral hydrate","chlorambucil","chloramphenicol","chlorcycloguanil","chlordiazepoxide","chlorhexidine","Chlorine containing products","chlormerodrin","chlormezanone","chlorocresol","chlorophyll","chloroprocaine","chloropyramine","chloroquine","chlorothiazide","chlorotrianisene","chloroxine","chlorphenesin","chlorpheniramine","chlorproguanil","chlorpromazine","chlorpropamide","chlorprothixene","chlorthalidone","chlorzoxazone","cholecalciferol","Cholera vaccines","cholestyramine","cholic acid","choline","Choline derivatives","Choline esters","CHOP","choriogonadotropin alfa","chromium","chymotrypsin","Cicatrizants","ciclesonide","ciclopirox","cidofovir","cilastatin","cilazapril","cilengitide","cilomilast","cilostazol","cimetidine","cinacalcet","cinalukast","cinitapride","cinnarizine","cinolazepam","cinoxacin","ciprofloxacin","cisapride","cisatracurium besylate","cisplatin","citalopram","citric acid","cladribine","clarithromycin","clavulanate","clemastine","clenbuterol","clidinium","clindamycin","clobazam","clobetasol","clocortolone","clodronate","clofarabine","clofazimine","clofibrate","clomifene","clomipramine","clomocycline","clonazepam","clonidine","clopidogrel","clorazepate","clotiazepam","clotrimazole","cloxacillin","clozapine","CMF","coagulation factor ix","coagulation factor viia","cobicistat","cobimetinib","cocaine","codeine","Cod-liver oil ointments","colchicine","Colchicine derivatives","colesevelam","colestipol","colistimethate","colistin","collagenase","colony stimulating factors","Colouring agents","Combinations and complexes of aluminium, calcium and magnesium compounds","Combinations for eradication of Helicobacter pylori","Combinations of adrenergics","Combinations Of Antibacterials","Combinations of antihistamines","Combinations Of Antihypertensives In Atc-gr. C02","Combinations of antineoplastic agents","Combinations of drugs for treatment of tuberculosis","Combinations of oral blood glucose lowering drugs","Combinations of penicillins, incl. beta-lactamase inhibitors","combinations of sulfonamides and trimethoprim, incl. derivatives","Combinations of vitamins","conivaptan","conjugated estrogens","Contact laxatives","Contraceptives For Topical Use","Contrast Media","copper","copper sulfate","coptisine","corn oil","Corticosteroid derivatives","corticosteroids","Corticosteroids And Antiinfectives In Combination","Corticosteroids and mydriatics in combination","Corticosteroids/antiinfectives/mydriatics in combination","Corticosteroids, combinations for treatment of acne","Corticosteroids, Combinations With Antibiotics","Corticosteroids, Combinations With Antiseptics","Corticosteroids, Dermatological Preparations","Corticosteroids For Systemic Use","Corticosteroids For Systemic Use, Combinations","Corticosteroids, moderately potent, combinations with antibiotics","Corticosteroids, moderately potent, combinations with antiseptics","Corticosteroids, moderately potent (group II)","Corticosteroids, moderately potent, other combinations","Corticosteroids, Other Combinations","Corticosteroids, potent, combinations with antibiotics","Corticosteroids, potent, combinations with antiseptics","Corticosteroids, potent (group III)","Corticosteroids, potent, other combinations","Corticosteroids, very potent, combinations with antibiotics","Corticosteroids, very potent, combinations with antiseptics","Corticosteroids, very potent (group IV)","Corticosteroids, very potent, other combinations","Corticosteroids, weak, combinations with antibiotics","Corticosteroids, weak, combinations with antiseptics","Corticosteroids, weak (group I)","Corticosteroids, weak, other combinations","corticotropin","cortisone acetate","Cosmetics","cosyntropin","Cough And Cold Preparations","Cough Suppressants And Expectorants, Combinations","Cough Suppressants, Excl. Combinations With Expectorants","coumarin","Coxibs","CP-800,569","creatine","Cremophor EL","crizotinib","cromoglicate","crotamiton","cryptenamine","Curare alkaloids","curcumin","cyanocobalamin","cyclacillin","cyclandelate","Cyclic amines","cyclizine","cyclobenzaprine","cyclopentolate","cyclophosphamide","cycloserine","cyclosporine","cyclothiazide","cycrimine","cyproheptadine","cyproterone","cysteamine","cytarabine","Cytotoxic Antibiotics And Related Substances","Dabigatran","dabigatran etexilate","dabrafenib","dacarbazine","daclatasvir","daclizumab","dacomitinib","dactinomycin","dalcetrapib","dalfopristin","dalteparin","danazol","daniquidone","dantrolene","Dantrolene and derivatives","dapagliflozin","dapiprazole","dapoxetine","dapsone","daptomycin","darapladib","darbepoetin alfa","darifenacin","darunavir","darunavir / ritonavir","dasabuvir","dasabuvir / ombitasvir / paritaprevir / ritonavir","dasatinib","daunorubicin","db-289","debrisoquine","decamethonium","decitabine","Decongestants And Antiallergics","Decongestants And Other Nasal Preparations For Topical Use","deferasirox","deferiprone","deferoxamine","defibrotide","degarelix","delavirdine","deleobuvir","demecarium bromide","demeclocycline","denileukin diftitox","denosumab","Dermatologicals","deserpidine","desflurane","desipramine","deslanoside","desloratadine","desmethylastemizole","desmethylcitalopram","desmopressin","desogestrel","desonide","desoximetasone","desoxycorticosterone pivalate","desvenlafaxine","Detoxifying agents for antineoplastic treatment","deutetrabenazine","dexamethasone","dexbrompheniramine","dexfenfluramine","dexibuprofen","dexketoprofen","dexlansoprazole","dexmedetomidine","dexmethylphenidate","dexrazoxane","dextran","dextroamphetamine","dextromethorphan","dextromethorphan / quinidine","dextropropoxyphene","dextrothyroxine","dezocine","Diagnostic Agents","Diagnostic Radiopharmaceuticals","Diaminopyrimidines","diatrizoate","diazepam","Diazepines, oxazepines and thiazepines","diazoxide","Dibenzo-bicyclo-octadiene derivatives","dibucaine","Dichloroacetamide derivatives","dichloroacetic acid","dichlorphenamide","diclofenac","dicloxacillin","dicumarol","dicyclomine","didanosine","dienestrol","Diet Formulations For Treatment Of Obesity","diethylcarbamazine","diethylpropion","diethylstilbestrol","diflomotecan","diflorasone","diflunisal","difluprednate","Digestives, Incl. Enzymes","digitalis glycosides","digitoxin","digoxin","digoxin immune fab","dihydrocodeine","dihydroergotamine","dihydroergotoxine","Dihydropyridine derivatives","dihydrotachysterol","dihydroxyaluminium","dilazep","diloxanide","diltiazem","dimenhydrinate","dimercaprol","dimethindene","dimethyl fumarate","dimethyl sulfoxide","dinoprost tromethamine","dinutuximab","Dipeptidyl peptidase 4 (DPP-4) inhibitors","diphemanil methylsulfate","diphenhydramine","diphenidol","diphenoxylate","Diphenylbutylpiperidine derivatives","Diphenylmethane derivatives","Diphenylpropylamine derivatives","diphenylpyraline","Diphtheria vaccines","dipivefrin","dipyridamole","dipyrone","direct acting antivirals","Direct thrombin inhibitors","dirithromycin","disopyramide","disulfiram","diuretics","Diuretics And Potassium-sparing Agents In Combination","divalproex sodium","divicine","dobutamine","docetaxel","docosanol","dodecane-trimethylamine","dofetilide","dolasetron","dolutegravir","dolutegravir / abacavir / lamivudine","domperidone","donepezil","Dopa and dopa derivatives","dopamine","Dopamine agonists","Dopaminergic Agents","dornase alfa","dorzolamide","dovitinib","doxacurium","doxapram","doxazosin","doxepin","doxorubicin","doxycycline","doxylamine","DPCPX","dromostanolone","dronabinol","dronedarone","droperidol","drospirenone","drospirenone / ethinyl estradiol","drotaverine","drotrecogin alfa","droxicam","droxidopa","Drugs acting on serotonin receptors","Drugs Affecting Bone Structure And Mineralization","Drugs For Acid Related Disorders","Drugs For Bile Therapy And Lipotropics In Combination","Drugs for embolisation","Drugs For Functional Bowel Disorders","Drugs For Functional Gastrointestinal Disorders","Drugs For Obstructive Airway Diseases","Drugs For Peptic Ulcer And Gastro-oesophageal Reflux Disease (gord)","Drugs For Treatment Of Bone Diseases","Drugs for treatment of hypercalcemia","Drugs for treatment of hyperkalemia and hyperphosphatemia","Drugs for treatment of hypoglycemia","Drugs For Treatment Of Lepra","Drugs For Treatment Of Tuberculosis","Drugs Used In Addictive Disorders","Drugs used in alcohol dependence","Drugs Used In Benign Prostatic Hypertrophy","Drugs Used In Diabetes","Drugs used in erectile dysfunction","Drugs used in nicotine dependence","Drugs used in opioid dependence","d-sorbitol","duloxetine","durvalumab","dutasteride","duvelisib","d-xylitol","dyclonine","dydrogesterone","dyphylline","e 7010","ebselen","ecabet","echinacea","echothiophate iodide","econazole","Ectoparasiticides, Incl. Scabicides","Ectoparasiticides, Incl. Scabicides, Insecticides And Repellents","eculizumab","edetic acid","edoxaban","edrophonium","efalizumab","efavirenz","efavirenz / emtricitabine / tenofovir disoproxil","egfr inhibitors","EKB-569","elacridar","elagolix","elbasvir","elbasvir / grazoprevir","electrolytes","Electrolyte solutions","Electrolytes With Carbohydrates","eletriptan","Elexacaftor","eliglustat","elosulfase alfa","eltrombopag","elvitegravir","elvitegravir / cobicistat / emtricitabine / tenofovir disoproxil fumarate","emapalumab","emedastine","Emollients And Protectives","empagliflozin","emtricitabine","enalapril","enasidenib","encainide","Encephalitis vaccines","encorafenib","Endocrine Therapy","endoxifen","Enemas","enflurane","enfuvirtide","enoxacin","enoxaparin","enoximone","enprofylline","entacapone","entecavir","enzalutamide","Enzyme and acid preparations, combinations","Enzyme inhibitors","Enzyme preparations","Enzymes","ephedra","ephedrine","epinastine","epinephrine","epipodophyllotoxin","epirubicin","eplerenone","epoetin alfa","Epoxides","eprosartan","eptifibatide","erdafitinib","ergocalciferol","ergoloid mesylate","ergonovine","Ergot alkaloids","Ergot alkaloids and oxytocin incl. analogues, in combination","ergotamine","eribulin","erlotinib","ertapenem","ertumaxomab","erythrityl tetranitrate","erythromycin","erythromycin ethylsuccinate / sulfisoxazole acetyl","escitalopram","eslicarbazepine","esmolol","esomeprazole","Esomeprazole / Naproxen","estazolam","Esters of aminobenzoic acid","Esters of benzoic acid","estradiol","estramustine","Estren derivatives","estriol","estrogens","Estrogens, combinations with other drugs","estrone","estropipate","eszopiclone","etanercept","eteplirsen","ethacrynic acid","ethambutol","ethanol","ethanolamine oleate","ethchlorvynol","ether","Ethers","Ethers chemically close to antihistamines","Ethers, chemically close to antihistamines","Ethers of tropine or tropine derivatives","ethinamate","ethinyl estradiol","ethinyl estradiol / norelgestromin","ethiodized oil","ethionamide","ethopropazine","ethosuximide","ethotoin","ethoxzolamide","Ethylene imines","ethynodiol diacetate","etidronic acid","etodolac","etomidate","etonogestrel","etoposide","etoricoxib","etravirine","etretinate","evacetrapib","everolimus","evodiamine","evolocumab","exemestane","exenatide","Expectorants","Expectorants, Excl. Combinations With Cough Suppressants","ezetimibe","ezetimibe / rosuvastatin","ezetimibe / simvastatin","faldaprevir","famciclovir","famotidine","fampridine","Farglitazar","farnesyltransferase inhibitors","fasudil","Fat/carbohydrates/proteins/minerals/vitamins, combinations","Fatty acid derivatives","febuxostat","fec protocol","felbamate","felbinac","felodipine","felypressin","Fenamates","fenbufen","fencamfamine","fenfluramine","fenofibrate","fenoldopam","fenoprofen","fenoterol","fentanyl","ferrous sulfate","fesoterodine","fevipiprant","fexofenadine","Fibrates","Fibrinogen","filgrastim","finasteride","firocoxib","First-generation cephalosporins","flavopiridol","flavoxate","flecainide","fleroxacin","flibanserin","flucloxacillin","fluconazole","flucytosine","fludarabine","fludiazepam","fludrocortisone","flufenamic acid","fluindione","flumazenil","flumethasone pivalate","flunarizine","flunisolide","flunitrazepam","flunoxaprofen","fluocinolone acetonide","fluocinonide","fluorescein","fluoride","fluorometholone","fluoroquinolones","fluorouracil","fluorouracil / salicylic acid","fluoxetine","fluoxetine / olanzapine","fluoxymesterone","flupenthixol","fluphenazine","flupirtine","flurandrenolide","flurazepam","flurbiprofen","fluspirilene","flutamide","fluticasone","fluticasone propionate","fluticasone/salmeterol","fluvastatin","fluvoxamine","FOLFIRI","FOLFOX","folic acid","folic acid analogues","Folic acid and derivatives","follitropin beta","fomepizole","fondaparinux sodium","forasartan","foretinib","formaldehyde","formic acid","formoterol","forskolin","fosamprenavir","fosamprenavir / ritonavir","fosaprepitant","foscarnet","fosfomycin","fosinopril","fosphenytoin","fospropofol","Fourth-generation cephalosporins","framycetin","frovatriptan","fructose","fructose 1,6 bisphosphate","fulvestrant","furafylline","furazolidone","furosemide","fusidic acid","gabapentin","gadobenate dimeglumine","gadobutrol","gadodiamide","gadofosveset trisodium","gadopentetate dimeglumine","gadoteridol","gadoversetamide","Gadoxetic acid","galactose","galantamine","gallamine triethiodide","gallium nitrate","galsulfase","gamma-homolinolenic acid","gamma hydroxybutyric acid","ganciclovir","Gangliosides and ganglioside derivatives","garlic oil","gatifloxacin","gefitinib","gelatin agents","geldanamycin","gemcitabine","gemcitabine triphosphate","gemcitabine triphosphate ditriethylamine","gemfibrozil","gemifloxacin","gemtuzumab ozogamicin","General Nutrients","genistein","Genito Urinary System And Sex Hormones","gentamicin","gentian violet","gepirone hydrochloride","gestodene","gilteritinib","ginkgo biloba","ginkgo biloba extract","ginseng","glatiramer acetate","glibenclamide","gliclazide","glimepiride","glipizide","gliquidone","glisoxepide","glucagon recombinant","Glucarpidase","glucocorticoids","gluconic acid","glucosamine","glucose","glutaraldehyde","glutethimide","glycerin","glycine","glycodiazine","Glycogenolytic Hormones","Glycopeptide antibacterials","glycopyrrolate","glycyl-sarcosine","gold preparations","gonadorelin","gonadotropin,chorionic","Gonadotropin releasing hormone analogues","Gonadotropin-releasing hormones","Gonadotropins","Gonadotropins And Other Ovulation Stimulants","goserelin","gramicidin d","granisetron","granulocyte colony-stimulating factor","grapefruit juice","grazoprevir","grepafloxacin","griseofulvin","GS-9350","guaifenesin","guanabenz","guanadrel sulfate","guanethidine","guanfacine","guanidine","Guanidine derivatives","Guanidine derivatives and diuretics","GW2016","Gynecological Antiinfectives And Antiseptics","H2-receptor antagonists","haemophilus b conjugate vaccine (prp-d-diphtheria toxoid conjugate)","halazepam","halobetasol propionate","halofantrine","Halogenated hydrocarbons","haloperidol","haloprogin","halothane","helium","hemin","Hemodialytics And Hemofiltrates","Hemodialytics, concentrates","Hemofiltrates","hemophilus influenzae b vaccines","heparin","Heparin group","Heparins or heparinoids for topical use","Hepatic And Reticulo Endothelial System","Hepatitis vaccines","heptabarbital","heroin","hesperetin","hesperidin","hetacillin","hexachlorophene","hexafluronium bromide","hexobarbital","hexocyclium","hexoprenaline","hexylcaine","High-ceiling Diuretics","High-ceiling diuretics and potassium-sparing agents","highly active antiretroviral therapy (haart)","histamine phosphate","hmg coa reductase inhibitors","HMG CoA reductase inhibitors in combination with other lipid modifying agents","HMG CoA reductase inhibitors, other combinations","homatropine methylbromide","homoharringtonine","hormonal contraceptives for systemic use","Hormone Antagonists And Related Agents","Hormones And Related Agents","hyaluronan","hyaluronidase","hydantoin derivatives","hydralazine","hydralazine / isosorbide dinitrate","Hydrazides","Hydrazinophthalazine derivatives","Hydrazinophthalazine derivatives and diuretics","hydrochlorothiazide","hydrocodone","hydrocortamate","hydrocortisone","hydroflumethiazide","hydrogen peroxide","hydromorphone","hydroquinidine","hydroquinone","hydroxocobalamin","hydroxychloroquine","hydroxyprogesterone","hydroxypropyl cellulose","Hydroxyquinoline derivatives","hydroxystilbamidine isethionate","hydroxytryptamine","hydroxyurea","hydroxyzine","hyoscyamine","hyperforin","Hypertonic solutions","Hypnotics And Sedatives","Hypnotics and sedatives in combination, excl. barbiturates","Hypothalamic Hormones","ibandronate","ibritumomab","ibrutinib","ibudilast","ibufenac","ibuprofen","ibutilide","icatibant","icodextrin","icosapent","icotinib","idarubicin","idoxuridine","idraparinux","idursulfase","ifosfamide","iguratimod","ilaprazole","iloperidone","iloprost","imatinib","imidapril","Imidazole and triazole derivatives","Imidazole derivatives","Imidazole derivatives and corticosteroids","Imidazoline derivatives","Imidazoline receptor agonists","Imidazoline receptor agonists in combination with diuretics","Imidazothiazole derivatives","imiglucerase","imipenem","imipramine","imiquimod","immune globulin","Immune Sera","Immune Sera And Immunoglobulins","Immunoglobulins","Immunoglobulins, normal human","Immunostimulants","Immunosuppressants","Incontinence equipment","indacaterol","indapamide","indecainide","Indifferent preparations","indinavir","Indium (111In) compounds","indocyanine green","Indole derivatives","indomethacin","Infant Formulas","Inflammation And Infection Detection","infliximab","Influenza vaccines","inotersen","inotuzumab ozogamicin","Insecticides And Repellents","insulin-aspart","insulin-detemir","insulin glargine","insulin-glargine","insulin-glulisine","insulin-lispro","insulin lyspro recombinant","insulin peglispro","insulin, porcine","insulin recombinant","Insulins And Analogues","Insulins and analogues for inhalation","Insulins and analogues for injection, fast-acting","Insulins and analogues for injection, intermediate-acting","Insulins and analogues for injection, intermediate-acting combined with fast-acting","Insulins and analogues for injection, long-acting","interferon alfa-2a, recombinant","interferon alfa-2b, recombinant","interferon alfacon-1","interferon alfa-n1","interferon alfa-n3","interferon beta-1a","interferon beta-1b","interferon gamma-1b","interferons","Interleukin inhibitors","Interleukins","Intermediate-acting sulfonamides","Intestinal Adsorbents","Intestinal Antiinfectives","Intestinal Antiinflammatory Agents","Intrauterine contraceptives","Intravaginal contraceptives","inulin","iobenguane (131i)","iodine","Iodine (123I) compounds","Iodine (125I) compounds","Iodine (131I) compounds","Iodine products","Iodine Therapy","iodipamide","iodixanol","iohexol","iophendylate","ipilimumab","ipratropium","iptakalim","irbesartan","irinotecan","iron","Iron bivalent, oral preparations","Iron chelating agents","iron dextran","Iron in combination with folic acid","Iron in other combinations","Iron Preparations","Iron trivalent, oral preparations","Iron trivalent, parenteral preparations","Irrigating Solutions","isocarboxazid","isoetharine","isoflurane","isoflurophate","isometheptene","isoniazid","isoniazid / pyrazinamide / rifampin","isopropamide","isopropyl alcohol","isoproterenol","isosorbide dinitrate","isosorbide mononitrate","isothipendyl","Isotonic solutions","isotretinoin","isoxicam","ispinesib mesylate","isradipine","itopride","itraconazole","ivabradine","ivacaftor","ivacaftor / lumacaftor","ivacaftor / tezacaftor","ivermectin","ivosidenib","I.v. Solution Additives","I.v. Solutions","ixabepilone","josamycin","kanamycin","kaolin","ketamine","ketanserin","ketazolam","ketoconazole","ketoprofen","ketorolac","ketotifen","kunecatechins","kyotorphin","labetalol","lacidipine","lacosamide","lactose","lactulose","lafutidine","l-alanine","lamivudine","lamivudine / abacavir","lamotrigine","lansoprazole","lanthanum carbonate","lapatinib","l-arginine","laronidase","laropiprant","larotrectinib sulfate","l-asparagine","l-aspartic acid","latamoxef","latanoprost","latonduine a","Laxatives","l-carnitine","l-citrulline","l-cysteine","l-cystine","lecithin","ledipasvir","ledipasvir / sofosbuvir","leflunomide","lenalidomide","lenvatinib","lepirudin","lercanidipine","lesinurad","letermovir","letrozole","leucovorin","Leukotriene receptor antagonists","leuprolide","levallorphan","levamisole","levetiracetam","levobunolol","levobupivacaine","levocabastine","levodopa","levofloxacin","levomefolic acid","levomepromazine","levomethadyl acetate","levomilnacipran","levonordefrin","levonorgestrel","levorphanol","levosimendan","levothyroxine","l-glutamic acid","l-glutamine","l-histidine","lidocaine","lidocaine and tetracaine","lidocaine / prilocaine","lidoflazine","lincomycin","Lincosamides","lindane","linezolid","liothyronine","liotrix","lipase","Lipid Modifying Agents","Lipid Modifying Agents, Combinations","Lipid Modifying Agents, Plain","lipoic acid","Liquid plasters","liraglutide","lisdexamfetamine","lisinopril","l-isoleucine","lisuride","lithium","liver extract","Liver therapy","Liver Therapy, Lipotropics","l-leucine","l-lysine","l-methyldopa","l-methylfolate","Local Anesthetics","Local hemostatics","lofexidine","lomefloxacin","lomitapide","lomustine","lonafarnib","Long-acting sulfonamides","loperamide","lopinavir","lopinavir / ritonavir","loracarbef","loratadine","lorazepam","Lorenzo's oil","lorlatinib","l-ornithine","lornoxicam","losartan","losigamone","loteprednol etabonate","lovastatin","Low-ceiling diuretics and potassium-sparing agents","Low-ceiling Diuretics, Excl. Thiazides","Low-ceiling Diuretics, Thiazides","Low-energy diets","loxapine","loxoprofen","l-phenylalanine","l-proline","l-serine","l-threonine","l-tryptophan","l-tyrosine","lubiprostone","lucanthone","lucitanib","lumacaftor","lumefantrine","lumiracoxib","Lung surfactants","lurasidone","lurbinectedin","lusutrombopag","lutropin alfa","l-valine","LY2140023","LY686017","lymecycline","Macrolides","Macrolides, Lincosamides And Streptogramins","mafenide","Magnesium","magnesium acetate","magnesium chloride","Magnesium compounds","magnesium gluconate","magnesium oxide","magnesium sulfate","magnesium trisilicate","Magnetic Resonance Imaging Contrast Media","malathion","mannitol","MAO inhibitors","MAO inhibitors and diuretics","maprotiline","maraviroc","marimastat","masitinib","masoprocol","maytansine","mazindol","Measles vaccines","mebendazole","mecamylamine","mecasermin","mechlorethamine","meclizine","meclofenamic acid","Medical gases","Medicated Dressings","Medicated dressings with antiinfectives","Medicated shampoos","medroxyprogesterone","medroxyprogesterone/conjugated estrogens","medrysone","mefenamic acid","mefloquine","megestrol","meglitinides","melacine(ribi immunochem)","melarsoprol","melatonin","Melatonin receptor agonists","meloxicam","melphalan","memantine","menadione","menadione sodium bisulfite","Meningococcal vaccines","menotropins","menthol","mepenzolate","meperidine","mephedrone","mephentermine","mephenytoin","mepivacaine","meprobamate","mepyramine","mequitazine","mercaptopurine","Mercurial diuretics","Mercurial products","meropenem","mesalazine","mesna","mesoridazine","mestranol","metabutethamine","metaraminol","metaxalone","metformin","methacholine","methacholine chloride","methacycline","methadone","methadyl acetate","methamphetamine","Methanolquinolines","methantheline","metharbital","methazolamide","methdilazine","methimazole","methionine","methocarbamol","methohexital","methotrexate","methotrimeprazine","methoxamine","methoxsalen","methoxyflurane","methoxyphenamine","methsuximide","methyclothiazide","methyl aminolevulinate","methyl-CCNU","methylcholanthrene","Methyldopa","Methyldopa and diuretics in combination","methylene blue","methylergonovine","Methylhydrazines","methylphenidate","methylphenobarbital","methylprednisolone","methylscopolamine","methyltestosterone","methyprylon","methysergide","meticillin","metipranolol","metixene","metoclopramide","metocurine","metolazone","metoprolol","metrizamide","metronidazole","metyrapone","metyrosine","mexiletine","mezlocillin","MI-63","mianserin","mibefradil","micafungin","miconazole","midazolam","midodrine","midostaurin","mifepristone","migalastat","miglitol","miglustat","Milk substitutes","milnacipran","milrinone","mimosine","minaprine","Mineralocorticoids","Mineral Supplements","minocycline","minoxidil","mipomersen","mirabegron","miroprofen","mirtazapine","misoprostol","mitiglinide","mitomycin","mitotane","mitoxantrone","mivacurium","mivacurium chloride","mizolastine","MK-571","MK-7246","moclobemide","modafinil","moexipril","molindone","molybdenum","mometasone","Monoamine oxidase A inhibitors","Monoamine oxidase B inhibitors","Monoamine oxidase inhibitors, non-selective","Monobactams","monobenzone","Monoclonal antibodies","montelukast","moricizine","Morphinan derivatives","morphine","motesanib","moviprep","moxifloxacin","MPP+","Mucolytics","Multivitamins, Combinations","Multivitamins, other combinations","Multivitamins, Plain","Multivitamins with minerals","Mumps vaccines","mupirocin","muraglitazar","muromonab","Muscle Relaxants","Muscle Relaxants, Centrally Acting Agents","Muscle Relaxants, Directly Acting Agents","muscle relaxants, peripherally acting agents","Musculo-skeletal System","myclobutanil","mycophenolate mofetil","mycophenolic acid","Mydriatics And Cycloplegics","nabilone","nabumetone","n-acetyl-d-glucosamine","n-acetyl serotonin","nadolol","nadroparin","nafarelin","nafcillin","naftifine","nalbuphine","nalidixic acid","nalmefene","naloxone","naltrexone","nandrolone","nandrolone decanoate","naphazoline","naphthol","naproxen","naratriptan","naringenin","naringin","Nasal Decongestants For Systemic Use","Nasal Preparations","natalizumab","natamycin","nateglinide","Natural and semisynthetic estrogens, plain","Natural opium alkaloids","navitoclax","nebivolol","nedocromil","nefazodone","nelarabine","nelfinavir","nemonapride","neomycin","neostigmine","nepafenac","Nepicastat","neratinib","Nerve depressants","nesiritide","netilmicin","Neuraminidase inhibitors","neuropsychiatric medications","nevirapine","NG-monomethyl-l-arginine","niacin","nicardipine","nicergoline","niclosamide","nicorandil","nicotine","Nicotinic acid and derivatives","nifedipine","niflumic acid","nilotinib","nilutamide","nilvadipine","nimesulide","nimodipine","niraparib","nisoldipine","nitazoxanide","nitisinone","nitrazepam","nitrendipine","nitric oxide","nitrile","Nitroferricyanide derivatives","Nitrofuran derivatives","nitrofurantoin","nitrofurazone","nitrogen","Nitrogen mustard analogues","nitroglycerin","Nitroimidazole derivatives","nitroprusside","Nitrosoureas","nitrous oxide","nitroxoline","nivolumab","nizatidine","n,n-dimethylacetamide","non-nucleoside reverse transcriptase inhibitors","nonoxynol-9","Non-selective beta-adrenoreceptor agonists","Non-selective Calcium Channel Blockers","non-selective monoamine reuptake inhibitors","Non-watersoluble X-ray contrast media","norelgestromin","norepinephrine","norethindrone","norfloxacin","norgestimate","norgestrel","nortriptyline","Noscapine","novobiocin","nppb","NS-398","Nucleoside and nucleotide reverse transcriptase inhibitors","nucleosides and nucleotides excl. reverse transcriptase inhibitors","nusinersen","nutlin-3","Nutrients without phenylalanine","nystatin","O6-(4-Bromothenyl)guanine","OC144-093","ochratoxin A","octreotide","Ocular Vascular Disorder Agents","ofatumumab","ofloxacin","olanzapine","olaparib","olaratumab","olmesartan","olopatadine","olsalazine","Oltipraz","omalizumab","ombitasvir","ombitasvir / paritaprevir / ritonavir","omega-3 polyunsaturated fatty acids","omeprazole","onartuzumab","ondansetron","Ophthalmological And Otological Preparations","Ophthalmologicals","Opioid anesthetics","opioids","Opioids in combination with antispasmodics","opipramol","Opium alkaloids and derivatives","Opium derivatives and expectorants","oprelvekin","Oral rehydration salt formulations","orange juice","orbofiban","orciprenaline","Organic acids","organic nitrates","Organophosphorous compounds","Oripavine derivatives","orlistat","orphenadrine","oseltamivir","osimertinib","Osmotically acting laxatives","ospa lipoprotein","ospemifene","otamixaban","Other Agents Acting On The Renin-angiotensin System","Other agents against amoebiasis and other protozoal diseases","Other agents against leishmaniasis and trypanosomiasis","Other agents for local oral treatment","Other agents for treatment of hemorrhoids and anal fissures for topical use","Other Alimentary Tract And Metabolism Products","Other alkylating agents","Other aminoglycosides","Other Anabolic Agents","Other Analgesics And Antipyretics","Other anterior pituitary lobe hormones and analogues","Other anti-acne preparations for systemic use","Other anti-acne preparations for topical use","Other antiallergics","Other Antianemic Preparations","Other Antibacterials","Other antibiotics for topical use","Other anticestodals","Other anti-dementia drugs","Other antidepressants","Other Antidiarrheals","Other antiemetics","Other antiepileptics","Other antifungals for topical use","Other antiglaucoma preparations","Other antigout preparations","Other antihistamines for systemic use","Other Antihypertensives","Other antihypertensives and diuretics","Other antiinfectives","Other antiinfectives and antiseptics","Other antiinflammatory and antirheumatic agents, non-steroids","Other antiinflammatory/antirheumatic agents in combination with other drugs","Other antiinflammatory therapeutic radiopharmaceuticals","Other antimalarials","Other antimigraine preparations","Other antimycotics for systemic use","Other antinematodals","Other Antineoplastic Agents","Other antiobesity drugs","Other anti-parathyroid agents","Other antipruritics","Other antipsoriatics for systemic use","Other antipsoriatics for topical use","Other antipsychotics","Other antiseptics and disinfectants","Other antispasmodics in combination with analgesics","Other antispasmodics in combination with psycholeptics","Other antithrombotic agents","Other antithyroid preparations","Other antitrematodal agents","Other antivirals","Other anxiolytics","Other bacterial vaccines","other beta-lactam antibacterials","Other blood glucose lowering drugs, excl. insulins","Other capillary stabilizing agents","Other cardiac combination products","Other cardiac glycosides","Other Cardiac Preparations","Other cardiac stimulants","Other cardiovascular system diagnostic radiopharmaceuticals","Other centrally acting agents","Other central nervous system diagnostic radiopharmaceuticals","Other cephalosporins","Other chemotherapeutics","Other cicatrizants","Other class I antiarrhythmics","Other Cold Combination Preparations","Other combinations of nutrients","Other cough suppressants","Other cough suppressants and expectorants","Other cytotoxic antibiotics","Other Dermatological Preparations","Other dermatologicals","Other Diagnostic Agents","Other Diagnostic Radiopharmaceuticals","Other diagnostic radiopharmaceuticals for inflammation and infection detection","Other diagnostic radiopharmaceuticals for tumour detection","Other Diuretics","Other dopaminergic agents","Other drugs affecting bone structure and mineralization","Other Drugs For Acid Related Disorders","Other drugs for bile therapy","Other Drugs For Disorders Of The Musculo-skeletal System","Other drugs for functional bowel disorders","Other Drugs For Obstructive Airway Diseases, Inhalants","Other drugs for peptic ulcer and gastro-oesophageal reflux disease (GORD)","Other drugs for treatment of tuberculosis","Other drugs used in benign prostatic hypertrophy","Other Drugs Used In Diabetes","Other ectoparasiticides, incl. scabicides","Other emollients and protectives","Other estrogens","Other general anesthetics","Other Gynecologicals","Other Hematological Agents","Other hem products","Other hepatic and reticulo endothelial system diagnostic radiopharmaceuticals","Other high-ceiling diuretics","Other hormone antagonists and related agents","Other hormones","Other hypnotics and sedatives","Other immunoglobulins","Other immunostimulants","Other immunosuppressants","Other insecticides and repellents","Other intestinal adsorbents","Other intestinal antiinfectives","Other irrigating solutions","Other i.v. solution additives","Other laxatives","Other lipid modifying agents","Other local anesthetics","Other low-ceiling diuretics","Other magnetic resonance imaging contrast media","Other mineral products","Other Mineral Supplements","Other muscle relaxants, peripherally acting agents","Other nasal preparations","Other Nervous System Drugs","Other non-selective calcium channel blockers","Other non-therapeutic auxiliary products","Other Nutrients","Other Ophthalmological And Otological Preparations","Other ophthalmological diagnostic agents","Other Ophthalmologicals","Other opioids","Other Otologicals","Other oxytocics","Other parasympathomimetics","Other peripheral vasodilators","Other Plain Vitamin Preparations","Other plant alkaloids and natural products","Other potassium-sparing agents","Other psychostimulants and nootropics","Other quaternary ammonium compounds","Other quinolones","Other renal system diagnostic radiopharmaceuticals","Other respiratory system diagnostic radiopharmaceuticals","Other Respiratory System Products","Other sclerosing agents","Other selective calcium channel blockers with mainly vascular effects","Other Sex Hormones And Modulators Of The Genital System","Other specific antirheumatic agents","Other surgical aids","Other Systemic Drugs For Obstructive Airway Diseases","Other systemic hemostatics","Other therapeutic products","Other Therapeutic Radiopharmaceuticals","Other topical products for joint and muscular pain","Other urologicals","Other Urologicals, Incl. Antispasmodics","Other Vaccines","Other vasodilators used in cardiac diseases","Other viral vaccines","Other Vitamin Products, Combinations","Otologicals","ouabain","Ovulation stimulants, synthetic","oxacillin","oxaliplatin","oxamniquine","oxandrolone","oxaprozin","oxatomide","oxazepam","Oxazolidine derivatives","Oxazol, thiazine, and triazine derivatives","oxcarbazepine","Oxicams","oxiconazole","oxprenolol","oxtriphylline","oxybenzone","oxybuprocaine","oxybutynin","oxycodone","oxygen","oxymetazoline","oxymetazoline and tetracaine","oxyphenbutazone","oxyphencyclimine","oxyphenonium","oxytetracycline","Oxytocics","oxytocin","Oxytocin and analogues","paclitaxel","pactimibe","Pain Palliation (bone Seeking Agents)","palbociclib","palifermin","paliperidone","palivizumab","palonosetron","pamaquine","pamidronate","Pancreatic Hormones","pancrelipase","pancreozymin (cholecystokinin)","pancuronium","panitumumab","panobinostat","pantoprazole","papain","papaverine","Papaverine and derivatives","Papillomavirus vaccines","Paracetamol, combinations excl. Psycholeptics (Vicks MediNait Sirup)","paraformaldehyde","Paramagnetic contrast media","paramethadione","paramethasone","Parasympathomimetics","Parathyroid Hormones And Analogues","parecoxib","pargyline","paricalcitol","paritaprevir","paromomycin","paroxetine","patisiran","pazopanib","pci-24781","pefloxacin","pegademase bovine","pegaptanib","pegaspargase","pegfilgrastim","peginterferon alfa-2a","peginterferon alfa-2b","pegloticase","pegvisomant","pembrolizumab","pemetrexed","pemirolast","pemoline","penbutolol","penciclovir","penicillamine","Penicillamine and similar agents","penicillin g","Penicillins with extended spectrum","penicillin v","pentagastrin","pentamidine","pentamidine isethionate","pentazocine","pentobarbital","pentolinium","pentosan polysulfate","pentostatin","pentoxifylline","pepsin","perazine","Perchlorates","perflutren","pergolide","perhexiline","perifosine","perindopril","Peripherally acting antiobesity products","Peripheral Vasodilators","Peritoneal Dialytics","permethrin","perospirone","Peroxides","perphenazine","Pertussis vaccines","pertuzumab","pesticides","PHA-665752","phenacemide","phenacetin","phenazepam","phenazopyridine","phencyclidine","phendimetrazine","phenelzine","phenformin","phenindamine","phenindione","pheniramine","phenmetrazine","phenobarbital","phenol","Phenol and derivatives","phenolsulfonphthalein","Phenothiazine derivatives","phenothiazines with aliphatic side-chain","phenoxybenzamine","phenprocoumon","phensuximide","phentermine","phentolamine","phenylacetic acid","Phenylalkylamine derivatives","phenylbutazone","phenylephrine","Phenylpiperidine derivatives","phenylpropanolamine","phenytoin","phosphates","phosphatidylserine","Phosphodiesterase inhibitors","phospholipids","Phosphonic acid derivatives","phosphoric acid","phosphorus","photodynamic therapy","physostigmine","phytonadione","picrotoxin","pilocarpine","pilsicainide","pimecrolimus","pimozide","pindolol","pioglitazone","pipazethate","pipecuronium","piperacillin","piperaquine","piperazine","Piperazine and derivatives","Piperazine derivatives","Piperidinedione derivatives","piperonyl butoxide","pipobroman","pipotiazine","pirbuterol","pirenzepine","piroxicam","pitavastatin","pitolisant","pitrakinra","Pituitary And Hypothalamic Hormones And Analogues","pivampicillin","pivmecillinam","Plague vaccines","Plant Alkaloids And Other Natural Products","Plasters","Platelet aggregation inhibitors excl. heparin","platinum","Platinum compounds","plerixafor","plicamycin","Pneumococcal vaccines","podofilox","podophyllotoxin derivatives","podophyllum","poliomyelitis vaccines","polyethylene glycol","polyethylene glycol 400","polyethylene glycol 6000","polyethylene glycol 8000","polymyxin b sulfate","Polymyxins","polysorbate 80","polystyrene sulfonate","polythiazide","ponatinib","porfimer","posaconazole","Posterior Pituitary Lobe Hormones","potassium","potassium acetate","potassium chloride","potassium gluconate","potassium iodide","potassium phosphate, incl. comb. with other potassium salts","Potassium-sparing Agents","PP2","practolol","pralidoxime","pramipexole","pramlintide","pranlukast","prasugrel","pravastatin","prazepam","praziquantel","prazosin","prednicarbate","prednisolone","prednisone","pregabalin","Pregnadien derivatives","Pregnen (4) derivatives","prenylamine","preotact","Preparations containing sulfur","Preparations for biliary tract therapy","Preparations For Treatment Of Wounds And Ulcers","Preparations increasing uric acid excretion","Preparations inhibiting uric acid production","Preparations with no effect on uric acid metabolism","Preparations with salicylic acid derivatives","pridopidine","prilocaine","primaquine","primidone","probenecid","probucol","procainamide","procaine","procarbazine","procaterol","prochlorperazine","procyclidine","proflavine","progabide","progesterone","Progestogens","Progestogens and estrogens, fixed combinations","progestogens and estrogens in combination","Progestogens and estrogens, sequential preparations","proguanil","Prolactine inhibitors","promazine","promethazine","propafenone","propantheline","proparacaine","propericiazine","propiconazole","propiomazine","propionic acid derivatives","propofol","propoxyphene","propranolol","Propulsives","propylhexedrine","propylthiouracil","Prostaglandin analogues","prostaglandin E2","prostaglandin I2","prostaglandins","protamine","protease inhibitors","Protectives Against Uv-radiation","Protectives against UV-radiation for systemic use","Protectives against UV-radiation for topical use","Proteinase inhibitors","Protein kinase inhibitors","protein supplements","Proteolytic enzymes","Proton pump inhibitors","protriptyline","pseudoephedrine","Psoralens for systemic use","Psoralens for topical use","Psychoanaleptics","Psycholeptics","Psycholeptics And Psychoanaleptics In Combination","Psychostimulants, Agents Used For Adhd And Nootropics","Psychostimulants in combination with psycholeptics","purine analogues","Purine derivatives","pyrazinamide","Pyrazolone derivatives","Pyrazolones","Pyrethrines","Pyrethrines, incl. synthetic compounds","pyrethrins and piperonyl butoxide","pyridostigmine","pyridoxal","pyridoxal phosphate","pyridoxine","pyrilamine","pyrimethamine","Pyrimidine analogues","Pyrimidine derivatives","pyruvic acid","qt-prolonging drugs","Quaternary ammonium compounds","quazepam","quetiapine","quinacrine","quinapril","quinestrol","quinethazone","quinidine","quinidine barbiturate","quinine","Quinine and derivatives","Quinoline derivatives","Quinoline derivatives and corticosteroids","Quinoline derivatives and related substances","Quinolines","Quinolone Antibacterials","Quinolone vasodilators","quinupristin","R101933","rabeprazole","rabies immunoglobulin","rabies vaccines","radiotherapy","raloxifene","raltegravir","raltitrexed","ramelteon","ramipril","ramucirumab","ranibizumab","ranitidine","ranolazine","rasagiline","rasburicase","Rauwolfia alkaloids","Rauwolfia alkaloids and diuretics in combination","reboxetine","reduced nicotinamide adenine dinucleotide","reduced nicotinamide adenine dinucleotide phosphate","regadenoson","regorafenib","remifentanil","remikiren","remoxipride","Renal System","Renin-inhibitors","repaglinide","rescinnamine","reserpine","Respiratory stimulants","Respiratory System","Resveratrol","retapamulin","reteplase","retigabine","retinal","Retinoids for topical use in acne","Retinoids for treatment of acne","Retinoids for treatment of psoriasis","rhodamine 123","ribavirin","ribociclib","riboflavin","ridaforolimus","ridogrel","rifabutin","rifampin","rifapentine","rifaximin","riluzole","rimantadine","rimexolone","rimonabant","riociguat","risedronate","risperidone","ritodrine","ritonavir","rituximab","rivaroxaban","rivastigmine","rizatriptan","rocuronium","rofecoxib","roflumilast","rolipram","rolitetracycline","romidepsin","ropinirole","ropivacaine","rosiglitazone","rosoxacin","rostafuroxin","rosuvastatin","Rota virus diarrhea vaccines","rotigaptide","rotigotine","rotigotine transdermal patch","roxatidine acetate","roxithromycin","Rubella vaccines","rucaparib","rufinamide","Rupatadine","ruxolitinib","ryanodine","s 1 (combination)","sacubitril","s-adenosylmethionine","salbutamol","salicylamide","salicylate-magnesium","salicylate-sodium","salicylic acid","Salicylic acid and derivatives","Salicylic acid derivatives","Salicylic acid preparations","salmeterol","salmon calcitonin","salsalate","Salt solutions","salvianolic acid b","saprisartan","saquinavir","saquinavir / ritonavir","saracatinib","sargramostim","satumomab pendetide","saxagliptin","SC-560","Scilla glycosides","Sclerosing agents for local injection","scopolamine","scutellarin","secobarbital","Secondary and tertiary amines","Second-generation cephalosporins","secretin","selective beta-2-adrenoreceptor agonists","Selective Calcium Channel Blockers With Direct Cardiac Effects","Selective Calcium Channel Blockers With Mainly Vascular Effects","Selective estrogen receptor modulators","Selective immunosuppressants","Selective serotonin (5HT1) agonists","Selective serotonin reuptake inhibitors","selegiline","selenium","selenium sulfide","selenium supplements","selumetinib","sematilide","semaxanib","Sensitivity tests, discs and tablets","Sensitizers used in photodynamic/radiation therapy","Sensory Organs","sergliflozin","sermorelin","Serotonin (5HT3) antagonists","Serotonin antagonists","Serotonin antagonists and diuretics","sertaconazole","sertindole","sertraline","sevelamer","sevoflurane","Sex Hormones And Modulators Of The Genital System","Short-acting sulfonamides","sibutramine","sildenafil","silibinin","silicone products","silodosin","Silver compounds","silver nitrate","silver sulfadiazine","simeprevir","simvastatin","sipoglitazar","siponimod","sirolimus","sitagliptin","sitamaquine","sitaxentan","SJG-136","Skeleton","(S)-methadone","sodium acetate","sodium ascorbate","sodium benzoate","sodium benzoate / sodium phenylacetate","sodium bicarbonate","sodium bisulfite","sodium carbonate","sodium chloride","sodium citrate","sodium ferulate","sodium fluoride","sodium lauryl sulfate","sodium nitrite","sodium phenylbutyrate","sodium phosphate","sodium selenite","sodium stibogluconate","sodium succinate","sodium sulfate","sodium tetradecyl sulfate","sodium valproate","sofosbuvir","sofosbuvir / velpatasvir","sofosbuvir / velpatasvir / voxilaprevir","soft paraffin dressings","solifenacin","solithromycin","Solutions affecting the electrolyte balance","Solutions for parenteral nutrition","Solutions producing osmotic diuresis","Solvents and diluting agents, incl. irrigating solutions","somatostatin","Somatropin and somatropin agonists","somatropin recombinant","sorafenib","sotalol","sparfloxacin","sparteine","Specific Antirheumatic Agents","Specific immunoglobulins","spectinomycin","spermine","spirapril","spironolactone","SR144528","stanozolol","starch","staurosporine","stavudine","stepronin","Steroid antibacterials","stiripentol","st. john's wort","Stomatological Preparations","Stomi equipment","Streptogramins","streptokinase","streptomycin","Streptomycins","streptozocin","Strophantus glycosides","Substituted alkylamines","Substituted ethylene diamines","succimer","Succinimide derivatives","succinylcholine","sucralfate","sucrose","sufentanil","sugar","sulfacetamide","sulfacytine","sulfadiazine","sulfadimethoxine","sulfadoxine","sulfamerazine","sulfamethazine","sulfamethizole","sulfamethoxazole","sulfamethoxazole / trimethoprim","sulfametopyrazine","sulfamoxole","sulfanilamide","sulfaphenazole","sulfapyridine","sulfasalazine","sulfathiazole","sulfinpyrazone","sulfisoxazole","sulfonamides","Sulfonamides and corticosteroids","Sulfonamides and potassium in combination","Sulfonamides And Trimethoprim","Sulfonamides, combinations with other drugs","Sulfonamides (heterocyclic)","sulfonamides, plain","sulfonamides, urea derivatives","Sulfonium derivatives","sulfoxone","sulfur","Sulfur-containing imidazole derivatives","Sulfur containing products","sulindac","sulodexide","sulpiride","sulthiame","sumatriptan","sunitinib","Superparamagnetic contrast media","suprofen","suramin","Surgical Aids","Surgical Dressings","suxibuzone","Sympathomimetics","Sympathomimetics, combinations excl. corticosteroids","Sympathomimetics excl. antiglaucoma preparations","Sympathomimetics in glaucoma therapy","Sympathomimetics, labour repressants","Sympathomimetics, plain","Sympathomimetics used as decongestants","Synthetic anticholinergic agents in combination with analgesics","Synthetic anticholinergic agents in combination with psycholeptics","Synthetic anticholinergics, esters with tertiary amino group","Synthetic anticholinergics, quaternary ammonium compounds","Synthetic antispasmodics, amides with tertiary amines","Synthetic estrogens, plain","Systemic Hormonal Preparations, Excl.","tacrine","tacrolimus","tadalafil","tafamidis","tafenoquine","tafluprost","talazoparib","talbutal","talinolol","talotrexin","tamibarotene","tamoxifen","tamsulosin","tanespimycin","tannic acid","tapentadol","Tariquidar","Tars","taselisib","tasosartan","taurine","taxanes","tazarotene","tazobactam","Technetium (99mTc) compounds","Technetium (99mTc), inhalants","technetium (99mtc) mertiatide","Technetium (99mTc), particles and colloids","Technetium (99mTc), particles for injection","technetium (99mtc) sulfur colloid","Technical disinfectants","tegafur","tegaserod","teicoplanin","telaprevir","telatinib","telbivudine","telcyta","telithromycin","telmisartan","temazepam","temozolomide","temsirolimus","tenecteplase","teniposide","tenofovir","tenoxicam","terazosin","terbinafine","terbutaline","terconazole","terfenadine","teriparatide","terlipressin","terodiline","Tertiary amines","terutroban","testolactone","testosterone","Testosterone-5-alpha reductase inhibitors","testosterone propionate","Tests for allergic diseases","Tests for bile duct patency","Tests for diabetes","Tests for fat absorption","Tests for fertility disturbances","Tests for gastric secretion","Tests for liver functional capacity","Tests for pancreatic function","Tests for pituitary function","Tests for renal function","Tests for thyreoidea function","tetanus antitoxin","tetanus toxoid","tetanus vaccines","tetrabenazine","tetracaine","tetracycline","Tetracycline and derivatives","Tetracyclines","tetrahydrobiopterin","tetrahydrofolic acid","Tetrahydropyrimidine derivatives","tezacaftor","thalidomide","theobromine","theophylline","Therapeutic Radiopharmaceuticals","thiabendazole","thiamine","thiamylal","thiazide derivatives","Thiazides and potassium in combination","Thiazides, combinations with other drugs","Thiazides, combinations with psycholeptics and/or analgesics","Thiazides, plain","thiazolidinediones","thiethylperazine","thioacetazone and isoniazid","Thiocarbamide derivatives","thioguanine","thiopental","thioproperazine","thioridazine","Thiosemicarbazones","thiotepa","thiothixene","Thiouracils","thioxanthene derivatives","Third-generation cephalosporins","Throat Preparations","thrombin","thymalfasin","thyroglobulin","thyroid hormones","thyroid preparations","Thyroid Therapy","thyrotropin","thyrotropin alfa","thyroxine","tiagabine","tianeptine","tiaprofenic acid","ticagrelor","ticarcillin","ticlopidine","tigecycline","Tilarginine Acetate","tiludronate","timolol","tinidazole","tinzaparin","tioconazole","tiotropium","tipifarnib","tipiracil hydrochloride","tipiracil / trifluridine","tipranavir","tipranavir / ritonavir","tirofiban","Tissue adhesives","tizanidine","tobramycin","tocainide","tocilizumab","tofisopam","tolazamide","tolazoline","tolbutamide","tolcapone","tolfenamic acid","tolmetin","tolnaftate","tolterodine","Tonics","Topical Products For Joint And Muscular Pain","topiramate","topoisomerase I inhibitors","topotecan","torasemide","torcetrapib","toremifene","tositumomab","trabectedin","tramadol","trametinib","trandolapril","tranexamic acid","tranilast","tranylcypromine","trastuzumab","trastuzumab emtansine","travoprost","trazodone","treprostinil","tretinoin","triadimefon","triamcinolone","triamterene","triazolam","Triazole derivatives","trichlormethiazide","trichloroacetic acid","trichloroethylene","trichostatin A","triciribine","tridihexethyl","trifluoperazine","triflupromazine","trifluridine","triflusal","triglycerides","trihexyphenidyl","trilostane","trimeprazine","trimethadione","trimethaphan","trimethobenzamide","trimethoprim","Trimethoprim and derivatives","trimetrexate","trimipramine","trioxsalen","tripelennamine","triprolidine","trisalicylate-choline","troglitazone","troleandomycin","trometamol","tropicamide","tropisetron","trospium","trovafloxacin","trypsin","tubastatin A","tubercidin","Tuberculosis diagnostics","Tuberculosis vaccines","tubocurarine","Tumor necrosis factor alpha (TNF-alpha) inhibitors","Tumour Detection","tyloxapol","tymazoline","Typhoid vaccines","Typhus (exanthematicus) vaccines","Tyrosine hydroxylase inhibitors","udenafil","Ultrasound Contrast Media","umeclidinium","umeclidinium / vilanterol","Unclassified","uracil mustard","urea","uridine","Urinary antispasmodics","Urinary concrement solvents","Urine Tests","urofollitropin","urokinase","Urologicals","ursodeoxycholic acid","ustekinumab","Vaccines","valaciclovir","valbenazine","valdecoxib","valganciclovir","valinomycin","valproic acid","valrubicin","valsartan","Valspodar","vancomycin","vandetanib","vanillin","vaniprevir","vapreotide","vardenafil","varenicline","Varicella zoster vaccines","Various","Various alimentary tract and metabolism products","Various diagnostic radiopharmaceuticals","Various pain palliation radiopharmaceuticals","Various therapeutic radiopharmaceuticals","Various thyroid diagnostic radiopharmaceuticals","Vasodilators Used In Cardiac Diseases","vasopressin","Vasopressin and analogues","Vasopressin antagonists","Vasoprotectives","vatalanib","vecuronium","vegetable oil","velaglucerase alfa","veliparib","velpatasvir","vemurafenib","venetoclax","venlafaxine","verapamil","vernakalant","verteporfin","Vicodin","vidarabine","vigabatrin","vilazodone","vildagliptin","vinblastine","vinca alkaloids and analogues","vincristine","vindesine","vinorelbine","vinyl chloride","Viral Vaccines","Viscoelastic substances","Vismodegib","vitamin a","Vitamin A And D, Incl. Combinations Of The Two","Vitamin A and D in combination","Vitamin A, plain","vitamin b12 and folic acid","Vitamin B12 (cyanocobalamin and analogues)","Vitamin B1 in combination with vitamin B6 and/or vitamin B12","Vitamin B1, plain","Vitamin B1, Plain And In Combination With Vitamin B6 And B12","Vitamin B-complex, Incl. Combinations","Vitamin B-complex, other combinations","vitamin b-complex, plain","Vitamin B-complex with anabolic steroids","Vitamin B-complex with minerals","Vitamin B-complex with vitamin C","vitamin c","vitamin d and analogues","vitamin e","Vitamin K","Vitamin K And Other Hemostatics","Vitamin K antagonists","Vitamins","Vitamins, other combinations","Vitamins with minerals","voacamine","voglibose","volatile anesthetics","voriconazole","vorinostat","vortioxetine","voxilaprevir","warfarin","Wart and anti-corn preparations","Washing agents etc.","Watersoluble, hepatotropic X-ray contrast media","Watersoluble, nephrotropic, high osmolar X-ray contrast media","Watersoluble, nephrotropic, low osmolar X-ray contrast media","wuzhi capsule","xanomeline","Xanthine derivatives","Xanthines","Xanthines and adrenergics","xanthophyll","XELOX","xenobiotics","xenon","ximelagatran","XK469","XR9051","X-ray Contrast Media, Iodinated","X-ray Contrast Media, Non-iodinated","xylometazoline","Yellow fever vaccines","yohimbine","Yttrium (90Y) compounds","zafirlukast","zalcitabine","zaleplon","zanamivir","zidovudine","zidovudine / lamivudine / abacavir","zileuton","zinc","zinc acetate","Zinc bandages","zinc oxide","Zinc products","zinc sulfate","ziprasidone","zoledronate","zolmitriptan","zolpidem","zomepirac","zonisamide","zopiclone","Zosuquidar","zoxazolamine","zuclopenthixol","Ace Inhibitors","adrenergics","Alkaloids","Amino acids/carbohydrates/minerals/vitamins","Androgen","Antiadrenergic Agents","Antiallergic agents","Antiarrhythmics","Antibiotics And Chemotherapeutics","Antidiarrheals","Antiinfectives And Antiseptics","Antiinflammatory preparations","Antiobesity Preparations","Antiparasitic Products","Antipruritics","Antispasmodics","Antivirals for treatment of HIV infections","Arteriolar Smooth Muscle","Ascorbic acid","Bacterial And Viral Vaccines","Barbiturates","Belladonna alkaloids","Belladonna And Derivatives","beta-lactam antibacterials","Blood Glucose Lowering Drugs","Blood tests","Blood transfusion","Carbohydrates/proteins/minerals/vitamins","Combinations and complexes of aluminium","Combinations of penicillins","combinations of sulfonamides and trimethoprim","Cough Suppressants And Expectorants","Cough Suppressants","CP-800","Diazepines","Digestives","Dipeptidyl peptidase 4","Drugs For Peptic Ulcer And Gastro-oesophageal Reflux Disease","Ectoparasiticides","Enzyme and acid preparations","Ergot alkaloids and oxytocin incl. analogues","Fat/carbohydrates/proteins/minerals/vitamins","fructose 1","gonadotropin","haemophilus b conjugate vaccine","Hemodialytics","highly active antiretroviral therapy","Hypnotics and sedatives in combination","Indium","insulin","Insulins and analogues for injection","interferon alfa-2a","interferon alfa-2b","iobenguane","Iron bivalent","Iron trivalent","Low-ceiling Diuretics","melacine","Monoamine oxidase inhibitors","Multivitamins","Natural and semisynthetic estrogens","Other antiinflammatory and antirheumatic agents","Other blood glucose lowering drugs","Other Drugs For Obstructive Airway Diseases","Other drugs for peptic ulcer and gastro-oesophageal reflux disease","Other ectoparasiticides","Other muscle relaxants","Other Vitamin Products","Ovulation stimulants","Oxazol","Pain Palliation","pancreozymin","Paracetamol","potassium phosphate","Pregnen","Progestogens and estrogens","Psychostimulants","s 1","Selective serotonin","Sensitivity tests","Serotonin","Solvents and diluting agents","Synthetic anticholinergics","Synthetic antispasmodics","Synthetic estrogens","Systemic Hormonal Preparations","Technetium","Thiazides","Tumor necrosis factor alpha","Typhus","Vitamin A And D","Vitamin B12","Vitamin B1","Vitamin B-complex","Watersoluble","X-ray Contrast Media","Yttrium"};
	public static String[] genes = {"TMB","MSI","ABI1","ABL1","ABL2","ACSL6","ACTB","ACVR1B","AF10","AF6","AFF1","AFF4","AKT1","AKT2","AKT3","ALK","ALOX12B","AMER1","AMER1","APC","APH1A","AR","ARAF","ARFRP1","ARHGAP26","ARHGEF12","ARID1A","ARID2","ARNT","ASMTL","ASXL1","ATF1","ATG5","ATIC","ATM","ATR","ATRX","AURKA","AURKB","AXIN1","AXL","B2M","BACH1","BAP1","BARD1","BCL10","BCL11A","BCL11B","BCL2","BCL2L1","BCL2L2","BCL3","BCL6","BCL7A","BCL8","BCL9","BCOR","BCORL1","BCR","BIRC3","BLM","BRAF","BRCA1","BRCA2","BRD4","BRIP1","BRSK1","BTG1","BTG2","BTK","BTLA","C11orf30","C11orf30","C17orf39","CAD","CALR","CAMTA1","CARD11","CARS","CASP8","CBFA2T3","CBFB","CBL","CCND1","CCND2","CCND3","CCNE1","CCT6B","CD22","CD274","CD274","CD36","CD58","CD70","CD74","CD79A","CD79B","CDC73","CDH1","CDK12","CDK4","CDK6","CDK8","CDKN1A","CDKN1B","CDKN2A","CDKN2B","CDKN2C","CDX2","CEBPA","CEP110","CHD2","CHEK1","CHEK2","CHIC2","CHN1","CIC","CIITA","CKS1B","CLP1","CLTC","CLTCL1","CNTRL","COL1A1","CPS1","CREB3L1","CREB3L2","CREBBP","CRKL","CRLF2","CSF1","CSF1R","CSF3R","CTCF","CTNNA1","CTNNB1","CUL3","CUL4A","CUX1","CXCR4","CYP17A1","DAXX","DDIT3","DDR1","DDR2","DDX10","DDX3X","DDX6","DEK","DIS3","DNM2","DNMT3A","DOT1L","DTX1","DUSP2","DUSP22","DUSP9","E2A","EBF1","ECT2L","EED","EGFR","EIF4A2","ELF4","ELL","ELN","ELP2","EML4","EMSY","ENL","EP300","EPHA3","EPHA5","EPHA7","EPHB1","EPHB4","EPOR","EPS15","ERBB2","ERBB3","ERBB4","ERCC4","ERG","ERRFI1","ESR1","ETO","ETS1","ETV1","ETV4","ETV5","ETV6","EWSR1","EXOSC6","EZH2","EZR","FAF1","FAM123B","FAM46C","FANCA","FANCC","FANCD2","FANCE","FANCF","FANCG","FANCL","FAS","FBXO11","FBXO31","FBXW7","FCGR2B","FCRL4","FEV","FGF10","FGF12","FGF14","FGF19","FGF23","FGF3","FGF4","FGF6","FGFR1","FGFR1OP","FGFR2","FGFR3","FGFR4","FH","FHIT","FLCN","FLI1","FLT1","FLT3","FLT4","FLYWCH1","FNBP1","FOXL2","FOXO1","FOXO3","FOXO4","FOXP1","FRS2","FSTL3","FUBP1","FUS","GABRA6","GADD45B","GAS7","GATA1","GATA2","GATA3","GATA4","GATA6","GID4","GID4","GLI1","GMPS","GNA11","GNA12","GNA13","GNAQ","GNAS","GPHN","GPR124","GRAF","GRIN2A","GRM3","GSK3B","GTSE1","H3F3A","HDAC1","HDAC4","HDAC7","HERPUD1","HEY1","HGF","HIP1","HIST1H1C","HIST1H1D","HIST1H1E","HIST1H2AC","HIST1H2AG","HIST1H2AL","HIST1H2AM","HIST1H2BC","HIST1H2BJ","HIST1H2BK","HIST1H2BO","HIST1H3B","HIST1H4l","HLF","HMGA1","HMGA2","HNF1A","HOXA11","HOXA13","HOXA3","HOXA9","HOXC11","HOXC13","HOXD11","HOXD13","HRAS","HSD3B1","HSP90AA1","HSP90AB1","ICK","ID3","IDH1","IDH2","IGF1R","IGH","IGK","IGL","IKBKE","IKZF1","IKZF2","IKZF3","IL21R","IL3","IL7R","INHBA","INPP4B","INPP5D","IRF1","IRF2","IRF4","IRF8","IRS2","ITK","JAK1","JAK2","JAK3","JARID2","JAZF1","JUN","KAT6A","KDM2B","KDM4C","KDM5A","KDM5C","KDM6A","KDR","KDSR","KEAP1","KEL","KIF5B","KIT","KLHL6","KMT2A","KMT2A","KMT2C","KMT2D","KMT2D","KRAS","LASP1","LCP1","LEF1","LMO1","LMO2","LPP","LRP1B","LRRK2","LTK","LYL1","LYN","MAF","MAFB","MAGED1","MALT1","MAP2K1","MAP2K1","MAP2K2","MAP2K2","MAP2K4","MAP3K1","MAP3K13","MAP3K14","MAP3K6","MAP3K7","MAPK1","MCL1","MDM2","MDM4","MDS2","MECOM","MED12","MEF2B","MEF2C","MEK1","MEK2","MEN1","MERTK","MET","MIB1","MITF","MKI67","MKL1","MKNK1","MLF1","MLH1","MLL","MLL2","MLL3","MLLT1","MLLT10","MLLT3","MLLT4","MLLT6","MMSET","MN1","MNX1","MPL","MRE11A","MSH2","MSH3","MSH6","MSI2","MSN","MST1R","MTAP","MTOR","MUC1","MUTYH","MYB","MYC","MYCL","MYCL","MYCL1","MYCN","MYD88","MYH11","MYH9","MYO18A","MYST3","NACA","NBEAP1","NBN","NCOA2","NCOR2","NCSTN","NDRG1","NF1","NF2","NFE2L2","NFKB2","NFKBIA","NIN","NKX2-1","NOD1","NOTCH1","NOTCH2","NOTCH3","NPM1","NR4A3","NRAS","NSD1","NSD2","NT5C2","NTRK1","NTRK2","NTRK3","NUMA1","NUP214","NUP93","NUP98","NUTM1","NUTM2A","OMD","P2RY8","PAFAH1B2","PAG1","PAK3","PALB2","PARK2","PARP1","PARP2","PARP3","PASK","PAX3","PAX5","PAX7","PBRM1","PBX1","PC","PCBP1","PCLO","PCM1","PCSK7","PD-1","PD-L1","PD-L2","PDCD1","PDCD1","PDCD11","PDCD1LG2","PDCD1LG2","PDCD1LG2PD-L2","PDE4DIP","PDGFB","PDGFRA","PDGFRB","PDK1","PER1","PHF1","PHF6","PICALM","PIK3C2B","PIK3C2G","PIK3CA","PIK3CB","PIK3CG","PIK3R1","PIK3R2","PIM1","PLAG1","PLCG2","PML","PMS2","POLD1","POLE","POT1","POU2AF1","PPARG","PPP1CB","PPP2R1A","PPP2R2A","PRDM1","PRDM16","PRKAR1A","PRKCI","PRKDC","PRRX1","PRSS8","PSIP1","PTCH1","PTEN","PTK7","PTPN11","PTPN2","PTPN6","PTPRO","QKI","RABEP1","RAC1","RAD21","RAD50","RAD51","RAD51B","RAD51C","RAD51D","RAD52","RAD54L","RAF1","RALGDS","RAP1GDS1","RARA","RASGEF1A","RB1","RBM10","RBM15","REL","RELN","RET","RHOA","RHOH","RICTOR","RNF213","RNF43","ROS1","RPL22","RPN1","RPTOR","RSPO2","RUNDC2A","RUNX1","RUNX1T1","RUNX2","S1PR2","SDC4","SDHA","SDHB","SDHC","SDHD","SEC31A","SEPT5","SEPT6","SEPT9","SERP2","SET","SETBP1","SETD2","SF3B1","SGK1","SH3GL1","SHIP","SHP-1","SLC1A2","SLC34A2","SMAD2","SMAD4","SMARCA1","SMARCA4","SMARCB1","SMC1A","SMC3","SMO","SNCAIP","SNX29","SOCS1","SOCS2","SOCS3","SOX10","SOX2","SOX9","SPEN","SPOP","SRC","SRSF2","SRSF3","SS18","SSX1","SSX2","SSX4","STAG2","STAT3","STAT4","STAT5A","STAT5B","STAT6","STK11","STL","SUFU","SUZ12","SYK","TAF1","TAF15","TAL1","TAL2","TBL1XR1","TBX3","TCF3","TCL1","TCL1A","TEC","TEK","TERC","TERT","TET1","TET2","TFE3","TFG","TFPT","TFRC","TGFBR2","TIPARP","TLL2","TLX1","TLX3","TMEM30A","TMPRSS2","TMSB4XP8","TMSL3","TNFAIP3","TNFRSF11A","TNFRSF14","TNFRSF17","TNFRSF6","TOP1","TP53","TP63","TPM3","TPM4","TRAF2","TRAF3","TRAF5","TRG","TRIM24","TRIP11","TSC1","TSC2","TSHR","TTL","TUSC3","TYK2","TYRO3","U2AF1","U2AF2","USP6","VEGFA","VHL","WDR90","WHSC1","WHSC1","WHSC1L1","WISP3","WT1","WTX","XBP1","XPO1","XRCC2","YPEL5","YY1AP1","ZBTB16","ZMYM2","ZMYM3","ZNF217","ZNF24","ZNF384","ZNF521","ZNF703","ZRSR2","ZSCAN3"};
	public static String[] meds = {"inhibitor","inhibitors","Abarelix","Abciximab","Abemaciclib","Abexinostat","Abiraterone","Acalabrutinib","Acetaminophen","Aclarubicin","Actinium Ac 225 lintuzumab","Acyclovir","Adenovirus-interferon","Ado-trastuzumab emtansine","Afatinib","Afuresertib","Aldesleukin","Alectinib","Alemtuzumab","Alendronate","Alisertib","All-trans retinoic acid","Allopurinol","Alpelisib","Alprazolam","Altretamine","Alvocidib","Amatuximab","AMG 330 in clinical trials","Amifostine","Aminocaproic acid","Aminoglutethimide","Aminopterin","Amonafide","Amoxicillin","Amrubicin","Amsacrine","Anagrelide","Anastrozole","Ancestim","Anti-inhibitor coagulant complex","Antithrombin III","Antithymocyte globulin","Apalutamide","Apatinib","Apixaban","Apocept","Aprepitant","Argatroban","Arsenic trioxide","Asciminib","Ascorbic acid","Asparaginase","Asparaginase Erwinia chrysanthemi","Aspirin","Aspirin and dipyridamole","Astuprotimut-R","Atezolizumab","Atropine","Atovaquone","Avapritinib","Avatrombopag","Avelumab","Axicabtagene ciloleucel","Axitinib","Azacitidine","Bacillus Calmette-Gu‚àö¬©rin","Barasertib","Bavituximab","bb2121 in clinical trials","Belagenpumatucel-L","Belinostat","Belotecan","Bendamustine","Benralizumab","Betrixaban","Bevacizumab","Bevacizumab-awwb","Bevacizumab-bvzr","Bexarotene","Bicalutamide","Binimetinib","Bivalirudin","BHQ880 in clinical trials","BL22 immunotoxin","Bleomycin","Blinatumomab","Bortezomib","Bosutinib","Brentuximab vedotin","Brigatinib","Buparlisib","Buserelin","Busulfan","Cabazitaxel","Cabozantinib","Calaspargase","Calcium phosphate rinse","Cangrelor","Capecitabine","Capivasertib","Caplacizumab","Capmatinib","Carboplatin","Carfilzomib","Carmustine","Carmustine wafer","Caspofungin","Catumaxomab","Cediranib","Cemiplimab","Ceritinib","Cetirizine","Cetuximab","Chidamide","Chlorambucil","Chlorozotocin","Chlorpheniramine","Cilostazol","Cimetidine","Ciprofloxacin","Cisplatin","Cixutumumab","Cladribine","Clarithromycin","Clemastine","Clodronate","Clofarabine","Clopidogrel","Cobimetinib","Coltuximab ravtansine","Copanlisib","Cortisone","Crenolanib","Crizanlizumab","Crizotinib","Custirsen","Cyanocobalamin","Cyclophosphamide","Cyclosporine modified","Cyclosporine non-modified","Cyproterone acetate","Cytarabine","Cytarabine and daunorubicin liposomal","Cytarabine liposomal","Cytomegalovirus Immune Globulin","Dabigatran","Dabrafenib","Dacarbazine","Dacomitinib","Dactinomycin","Dalteparin","Danazol","Dapsone","Daratumumab","Daratumumab and hyaluronidase","Darbepoetin alfa","Darolutamide","Dasatinib","Daunorubicin","Daunorubicin liposomal","Decitabine","Deferasirox","Deferiprone","Deferoxamine","Defibrotide","Degarelix","Denileukin diftitox","Denintuzumab mafodotin","Denosumab","Desmopressin","Dexamethasone","Dexchlorpheniramine","Dexrazoxane","Diethylstilbestrol","Dinaciclib","Dinutuximab","Diphenhydramine","Dipyridamole","Discodermolide","DMUC5754A in clinical trials","Docetaxel","Docusate","Dolasetron","Domperidone","Dovitinib","Doxifluridine","Doxorubicin","Pegylated liposomal doxorubicin","Doxycycline","Dronabinol","Durvalumab","Dutasteride","Duvelisib","Eculizumab","Edoxaban","Edrecolomab","Elotuzumab","Eltrombopag","Emapalumab","Emicizumab-kxwh","Emepepimut-S","Enasidenib","Encorafenib","Enfortumab vedotin","Enoxaparin","Ensartinib","Entinostat","Entospletinib","Entrectinib","Enzalutamide","Epirubicin","Epoetin alfa","Epoetin alfa-epbx","Epratuzumab","Eptifibatide","Erdafitinib","Eribulin","Erlotinib","Estradiol","Estramustine","Etirinotecan pegol","Etoposide","Everolimus","Exemestane","Factor VIIa","Factor VIII","Factor IX","Factor X","Factor Xa","Factor XIII concentrate","Famciclovir","Famotidine","Fam-trastuzumab deruxtecan","Fedratinib","Ferric carboxymaltose","Ferric gluconate","Ferrous sulfate","Ferumoxytol","Fibrinogen concentrate","Filanesib","Filgrastim","Filgrastim-aafi","Filgrastim-sndz","Finasteride","Fluorouracil","Floxuridine","Fluconazole","Fludarabine","Fluoxymesterone","Flutamide","Folic acid","Folinic acid","Fondaparinux","Formestane","Forodesine","Fosaprepitant","Fostamatinib","Fotemustine","Fruquintinib","Fulvestrant","Furosemide","Galeterone","Galunisertib","Ganetespib","Ganitumab","Gefitinib","Gemcitabine","Gemcitabine elaidate","Gemtuzumab ozogamicin","Gilteritinib","Glasdegib","Glembatumumab vedotin","Glucarpidase","Goserelin","Granisetron","Guadecitabine","Haloperidol","Hematopoetic progenitor cells","Heptaplatin","HER2 peptide vaccine","Histrelin","Hu5F9-G4 in clinical trials","Hydrocortisone","Hydroxyurea","Ibandronate","Ibritumomab tiuxetan","Ibrutinib","Icotinib","Idarubicin","Idarucizumab","Idasanutlin","Idelalisib","Ifosfamide","IMA901 in clinical trials","Imatinib","Imetelstat","Indatuximab ravtansine","Indomethacin","Infigratinib","Inotuzumab ozogamicin","Interferon alfa-2a","Interferon alfa-2b","Interferon gamma-1b","Iobenguane I 131","Iodine-131","Ipatasertib","IPH 2101 in clinical trials","Ipilimumab","Irinotecan","Irinotecan liposome","Iron dextran","Iron sucrose","Isatuximab","Isotretinoin","Itraconazole","Ivosidenib","Ixabepilone","Ixazomib","JCAR015 in clinical trials","Ketoconazole","Lactulose","Lamivudine","Lanreotide","Lansoprazole","Lapatinib","Lapuleucel-T","Larotrectinib","Lasofoxifene","Lenalidomide","Lenograstim","Lenvatinib","Lepirudin","Lestaurtinib","Letermovir","Letrozole","Leuprolide","Levamisole","Levofloxacin","Levoleucovorin","L-glutamine","Linifanib","Linsitinib","Lipefilgrastim","Lobaplatin","Lomustine","Loperamide","Lorazepam","Lorlatinib","Lorvotuzumab mertansine","Luspatercept","Lusutrombopag","Lutetium Lu 177 dotatate","LY3023414 in clinical trials","Mannitol","Mapatumumab","Masitinib","Mechlorethamine","Medroxyprogesterone","Megestrol","Melphalan","Meperidine","Mepolizumab","Mercaptopurine","Mesna","Methotrexate","Methoxsalen","Methylprednisolone","Metoclopramide","Midostaurin","Mifamurtide","Milataxel","Mirvetuximab soravtansine","Mitomycin","Mitotane","Mitoxantrone","MK2206 in clinical trials","Mocetinostat","Mogamulizumab","Momelotinib","MOR208 in clinical trials","Motesanib","Moxetumomab pasudotox","Mycophenolate mofetil","Nabilone","Necitumumab","Nedaplatin","Nelarabine","NEOD001","Neratinib","Netupitant and palonosetron","Nilotinib","Nilutamide","Nimustine","Nintedanib","Niraparib","Nivolumab","Nolatrexed","Non-pegylated liposomal doxorubicin","Norethandrolone","NovoTTF-100A system","Obinutuzumab","Octreotide","Octreotide LAR","Ofatumumab","Olanzapine","Olaparib","Olaptesed pegol","Olaratumab","Omacetaxine","Omeprazole","Onartuzumab","Ondansetron","Oprelvekin","Oprozomib","Orteronel","Osimertinib","Osocimab","Otlertuzumab","Oxaliplatin","Paclitaxel","Pacritinib","Palbociclib","Palifermin","Palonosetron","Pamidronate","Panitumumab","Panobinostat","Pantoprazole","Pazopanib","Pegaspargase","Pegfilgrastim","Pegfilgrastim-cbqv","Pegfilgrastim-jmdb","Peginterferon alfa-2a","Peginterferon alfa-2b","Pembrolizumab","Pemetrexed","Pemigatinib","Penicillin V","Pentamidine","Pentostatin","Pentraxin 2","Perifosine","Pertuzumab","Pexidartinib","Phenytoin","Phosphomannopentaose sulfate","Phytonadione","Pictilisib","Pidilizumab","Pinatuzumab vedotin","Pirarubicin","Pixantrone","Plerixafor","Plicamycin","Plinabulin","Polatuzumab vedotin","Pomalidomide","Ponatinib","Porfimer","Pracinostat","Pralatrexate","Prasugrel","Pravastatin","Prednisone","Prednisolone","Procarbazine","Prochlorperazine","Promethazine","Protamine sulfate","Prothrombin Complex Concentrate","Quinine","Quisinostat","Quizartinib","Rabeprazole","Radium Ra 223","Radotinib","Raloxifene","Raltitrexed","Ramosetron","Ramucirumab","Ranimustine","Ranitidine","Rasburicase","Ravulizumab","Realgar-Indigo naturalis formulation","Refametinib","Regorafenib","Relugolix","Reovirus","Retaspimycin","Rho","Ribociclib","Ricolinostat","Ridaforolimus","Rilotumumab","Ripretinib","Risedronate","Rituximab","Rituximab-abbs","Rituximab-pvvr","Rituximab and hyaluronidase human","Rivaroxaban","Rociletinib","Rolapitant","Romidepsin","Romiplostim","Ropeginterferon alfa-2b","Rucaparib","Ruxolitinib","Sacituzumab govitecan","Samarium-153","Sapacitabine","Sapanisertib","Sargramostim","Scopolamine","Seliciclib","Selinexor","Selpercatinib","Selumetinib","Semuloparin","Semustine","Sennosides","Siltuximab","Sipuleucel-T","Sirolimus","Sonidegib","Sorafenib","Spebrutinib","Streptozocin","Strontium-89","Sunitinib","Surufatinib","Sutimlimab","Tabalumab","Tacrolimus","Tagraxofusp","Talazoparib","Talimogene laherparepvec","Tamibarotene","Tamoxifen","Tazemetostat","Tbo-filgrastim","Tegafur and uracil","Tegafur","Telotristat","Temozolomide","Temsirolimus","Teniposide","Tesetaxel","Tesevatinib","Thalidomide","Thioguanine","Thiotepa","Ticagrelor","Ticlodipine","Tigatuzumab","Tinzaparin","Tipifarnib","Tirabrutinib","Tirofiban","Tisagenlecleucel","Tivantinib","Tivozanib","Tocilizumab","Tofacitinib","Topotecan","Toremifene","Tosedostat","Tositumomab & I-131","Trabectedin","Trametinib","Tranexamic acid","Trastuzumab","Trastuzumab-anns","Trastuzumab-dkst","Trastuzumab-dttb","Trastuzumab-pkrb","Trastuzumab-qyyp","Trastuzumab and hyaluronidase","Trebananib","Tremelimumab","Treosulfan","Trifluridine and tipiracil","Trimethoprim-Sulfamethoxazole","Triptorelin","Tropisetron","Tucatinib","Ublituximab","Umbralisib","Unfractionated heparin","Uracil mustard","Uridine triacetate","Vadastuximab talirine","Valacyclovir","Valganciclovir","Valproate","Valrubicin","Vandetanib","Varlilumab","Veliparib","Veltuzumab","Vemurafenib","Venetoclax","Vinblastine","Vincristine","Vincristine liposomal","Vindesine","Vinflunine","Vinorelbine","Vismodegib","Volasertib","von Willebrand factor and factor VIII complex","von Willebrand factor","Vorapaxar","Voriconazole","Vorinostat","Vosaroxin","Voxelotor","Voxtalisib","Warfarin","Zanubrutinib","Ziv-aflibercept","Zoledronic acid"};
	public static String folder = "/Users/m179121/Downloads/";
	public static String folderOut = "/Users/m179121/Downloads/";
	
    public static void main(String[] args) throws IOException, ParseException, ParserConfigurationException, SAXException, java.text.ParseException {
    	
//    	parseJSON(folder+"assertions.json");
//    	printArrayListFile(out, folderOut+"out.txt");
    	
//    	readXML(folder+"ClinVarTrait.xml");
//    	readXML(folder+"ClinVarFullRelease_2020-09.xml");
//    	splitDoc(folder+"ClinVarFullRelease_2020-02.xml");
//    	readTXT(folder+"ClinVarFullRelease_2020-02.xml");
//    	mapClinAnno("H:\\foundation\\genetics_results\\RWD\\temp.txt");
//    	varAnnPheno("H:\\GA4GH\\data\\annotations\\var_pheno_ann.tsv");
//    	varAnn("H:\\GA4GH\\data\\annotations\\var_fa_ann.tsv");
//    	varAnnExtract(folder+"in.txt");
//    	varAnnTrain(folder+"in.txt");
//    	clinicalAnn("H:\\foundation\\genetics_results\\RWD\\temp.txt");
    	
//    	varAnnFoundation(folder+"in.txt");
//    	varAnnUMLS(folder+"in.txt");
//    	UMLSCategoy(folder+"in.txt");
    	countType(folder+"in.txt");
//    	getGene(folder+"in.txt");
//    	getMed(folder+"in.txt");
//    	countWords(folder+"in.txt");
    	
//    	removeDuplicates(out);
//    	System.out.print(out.size());
    	printArrayListFile(out, folderOut+"out.txt");
    	
    }

    public static void readXML(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
    	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	    	String line = "";
	    	
	    	while ((line = br.readLine()) != null) {
	    		Pattern pat = Pattern.compile("\\b(clinical benefit|dose|dosage|response|metabolism|clearance|concentration(s)?|resistance|exposure|discontinuation|activity|affinity|catalytic activity|clearance|concentrations|enzyme activity|expression|formation|glucuronidation|half-life|inhibition|metabolism|protein stability|sensitivity|steady-state level|sulfation|transcription|transport|uptake)\\b");
				Matcher mat = pat.matcher(line);
	        	if(mat.find()) {
	        		System.out.println(mat.group()+"\t"+line.trim());
	        		out.add(line+"\t"+mat.group());
	        	}
	    	}
        	
//	         File inputFile = new File(file);
//	         DocumentBuilderFactory dbFactory = DocumentBuilderFactory.newInstance();
//	         DocumentBuilder dBuilder = dbFactory.newDocumentBuilder();
//	         org.w3c.dom.Document doc = dBuilder.parse(inputFile);
//	         doc.getDocumentElement().normalize();
//	         System.out.println("Root element :" + doc.getDocumentElement().getNodeName());
//
//	         NodeList nList = doc.getChildNodes();
//	         for (int temp = 0; temp < nList.getLength(); temp++) {
//	        	 Node nNode = nList.item(temp);
//	        	 if (nNode.getNodeType() == Node.ELEMENT_NODE) {
//	        		 System.out.println(nNode.getNodeName());
//	        		 out.add(nNode.getNodeName());
//	        	 }
//	         }
//	         
//	         NodeList nList = doc.getElementsByTagName("Trait");
//	         for (int temp = 0; temp < nList.getLength(); temp++) {
//	        	String relation = "";
//	            NodeList nList1 = nList.item(temp).getChildNodes();
//	            for (int temp1 = 0; temp1 < nList1.getLength(); temp1++) {
//		            Node nNode = nList1.item(temp1);
//		            if (nNode.getNodeType() == Node.ELEMENT_NODE) {
//		            	System.out.println(nNode.getNodeName());
//		            	if(nNode.getNodeName().equals("Name")) {
//				               Element eElement = (Element) nNode;
//				               String drugName = eElement.getTextContent().trim();
//				               relation = drugName;
//		            	}
//		            	else if(nNode.getNodeName().equals("TraitRelationship")) {
////	            		else if(nNode.getNodeName().equals("TraitRelationship")&&!((Element) nNode).getAttribute("Type").contains("Disease")) {
//		            		   Node nNode1 = nNode.getChildNodes().item(1);
//				               Element eElement = (Element) nNode1;
//				               String TraitRelationship = eElement.getTextContent().trim();
//				               relation = relation + "\t" + ((Element) nNode).getAttribute("Type") + "\t" + TraitRelationship;
//		            	}
//		            }
//	            }
//	            
//	            if(relation.split("\t").length>1) {
//	            	 out.add(relation);
//	            }
//	         }
	    }
    }
    
    public static void splitDoc(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
    	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
	        String print = "N";
	        int i = 0;
	        PrintWriter writer = null;
	        while ((line = br.readLine()) != null) {
//        		String mrn = line.split("\t")[0];
//	        	id.put(mrn, race+"\t"+ethn+"\t"+death);
	        	
	        	if(line.contains("<ClinVarSet")) {
	        		print = "Y";
	        		String id = line.substring(line.indexOf("ID=")+4, line.length()-2);
	        		writer = new PrintWriter(folder+"ClinVar\\"+ id +".txt", "UTF-8");
	        	}
	        	else if (line.contains("</ClinVarSet>")&&print.equals("Y")){
	        		i++;
//	        		out.add(line);
		        	writer.println(line.replaceAll("\\s{2,}", " "));
		        	writer.flush();
	        		print = "N";
	        	}
//	        	if(i>10000) {
//	        		break;
//	        	}
//	        	else{ 
	        		if(print.equals("Y")) {
//        			if(line.toLowerCase().contains("response")) {
	        			System.out.println(line.trim());
//	            		out.add(line);
	            		writer.println(line.replaceAll("\\s{2,}", " "));
	    	        	writer.flush();
	        		}
//	        	}
	        }
	        writer.close();
	    }
    }
    
   public static void mapClinAnno(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
    	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
    	    
	        while ((line = br.readLine()) != null) {
	        	
	        	String[] IDs = line.split("\t")[0].replace("\"", "").split(",");
	        	String phenotype = ".";
	        	if(line.split("\t").length>1) {
	        		phenotype = line.split("\t")[1];
	        	}
	        	System.out.println(phenotype);
	        	for(String i : IDs) {
	        		id.put(i, phenotype);
	        	}
	        }
	    }
	    
	    try (BufferedReader br = new BufferedReader(new FileReader("H:\\foundation\\genetics_results\\RWD\\out.txt"))) {
	    	
	        String line = "";
    	    
	        while ((line = br.readLine()) != null) {
	        	out.add(line+"\t"+id.get(line));
	        	System.out.println(line+"\t"+id.get(line));
	        }
	    }
	    
    }
   
   public static void varAnnTrain(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	String Sentence = line.replace("of$", "of $").replace("to$", "to $").replace("GENOMOD", "").replace("is ", "").replace("are ", "").replace("not ", "").replace("associated with", "associated").replace("as compared to", "compared").replace("when treated with", "treated").replace("when assayed with", "assayed").replace("when exposed to", "exposed");
	        	
	        	for(String w:Sentence.split(" ")) {
	        		if(w.contains("GENO$")) {
	        			Sentence = Sentence.replace(w,"GENO");
		        	}
	        		if(w.contains("CHEM$")) {
	        			Sentence = Sentence.replace(w,"CHEM");
		        	}
	        		if(w.contains("DISE$")) {
	        			Sentence = Sentence.replace(w,"DISE");
		        	}
	        		if(w.contains("PHENO$")) {
	        			Sentence = Sentence.replace(w,"PHENO");
		        	}
	        		if(w.contains("POPU$")) {
	        			Sentence = Sentence.replace(w,"POPU");
		        	}
	        		if(w.contains("GENE$")) {
	        			Sentence = Sentence.replace(w,"GENE");
		        	}
	        	}
	        	
	        	int i = searchedWord(Sentence, "POPU");
	        	String[] words = Sentence.split(" ");
	        	System.out.println(line);
	        	System.out.println(Sentence);
	        	String vec = "";
	        	if(i==-1) {
	        		continue;
	        	}
	        	if(i-2>=0&&i+2<words.length) {
		        	vec = words[i-2]+ " " + words[i-1]+ " " + words[i+1]+ " " + words[i+2];
	        	}
	        	else if(i+1<words.length) {
		        	vec = words[i-2]+ " " + words[i-1]+ " " + words[i+1];
	        	}
	        	else if(i<words.length) {
		        	vec = words[i-2]+ " " + words[i-1];
	        	}
	        	System.out.println(vec.replace("PHENO", "").replace("  ", " "));
	        	out.add(vec.replace("PHENO", "").replace("  ", " "));
	        }
	    }
   }
   
   public static void varAnnExtract(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
 	    
	        while ((line = br.readLine()) != null) {
	        	String Sentence = line.replace("of$", "of $").replace("to$", "to $");
	        	
	        	String condition = ".";
//       		Pattern pat = Pattern.compile("of \\$([A-Z0-9]{1,})(_protein|_mRNA)?\\|(GENO|CHEM)\\$");
//   			Matcher mat = pat.matcher(Sentence);
//	        	while(mat.find()) {
////       			condition = mat.group(1).trim();
//					if(mat.group(2)!=null) {
//						condition = mat.group(1)+mat.group(2);
//					}
//					else condition = mat.group(1);
//					
////					out.add(condition);
//			 		Sentence = Sentence.replace(condition+"|GENO", condition+"|GENE").replace(condition+"|CHEM", condition+"|GENE");
//	        	}
	        	
	        	
//	        	System.out.println(Sentence);
//	        	Pattern pat = Pattern.compile("\\$([A-Za-z0-9,_-]{1,})\\|CHEM\\$");
//	        	Matcher mat = pat.matcher(Sentence);
//	        	while(mat.find()) {
//       			condition = mat.group(1).trim();
//					out.add(condition);
//					System.out.println(condition);
//	        	}
	        	
	        	String sem = getSem(Sentence);
	        	
	        	out.add(sem.split("\t")[1]);

	        }
	    }
  }
   
   public static void varAnn(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
   	    
	        while ((line = br.readLine()) != null) {
	        	String Annotation_ID = line.split("\t")[0];
	        	String Gene = line.split("\t")[2].replace("\"", "");
	        	String Chemical = line.split("\t")[3].replace("\"", "");
	        	String Phenotype = line.split("\t")[5].replace("\"", "");
	        	String Sentence = line.split("\t")[8].replace("with as", "as").replace(" + ", "+").replace(" *", "*").replaceAll("\\b(genotype|genotypes|Genotypes)\\b", "Genotype").replace("allele", "Allele");
	        	String Genotype = "";
	        	if(line.split("\t").length>10) {
	        		Genotype = line.split("\t")[10].replace(" + ", "+").replace(" *", "*");
	        	}
	        	
	        	if(Sentence.endsWith(".")) {
	        		Sentence = Sentence.substring(0, Sentence.length()-1);
				}
	        	
	        	//GENO
	        	Sentence = annotateGenotype(Sentence, Genotype, Gene);
	        	
	        	//CHEM
	        	Sentence = annotateChemical(Sentence, Chemical);
	        	
	        	String pheno = ".";
	        	String aspect = ".";
	        	//va_drug_ann
        		Pattern pat = Pattern.compile("\\b(decreased |increased |reduced |positive |poorer |better |worse |shorter |longer )?(steady-state |trough |non-|ultra-)?(clinical benefit|dose|response|metabolism|clearance|concentration(s)?|resistance|exposure|discontinuation)\\b");
    			Matcher mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(mat.group(1)!=null) {
	        			aspect = mat.group(1).trim();
	        			if(mat.group(2)!=null) {
		        			pheno = mat.group(2).trim()+" "+mat.group(3).trim();
		        		}
	        			else pheno = mat.group(3).trim();
	        		}
	        		else pheno = mat.group();
//	        		out.add(Phenotype+"\t"+mat.group());
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
	        	}

	        	//va_fa_ann
//        		pat = Pattern.compile("\\b(decreased |increased |reduced |positive |poorer |better |worse |shorter |longer )?(activity|affinity|catalytic activity|clearance|concentrations|enzyme activity|expression|formation|glucuronidation|half-life|inhibition|metabolism|protein stability|sensitivity|steady-state level|sulfation|transcription|transport|uptake)\\b");
//    			mat = pat.matcher(Sentence);
//	        	while(mat.find()) {
//	        		if(mat.group(1)!=null) {
//	        			aspect = mat.group(1).trim();
//	        			pheno = mat.group(2).trim();
//	        		}
//	        		else pheno = mat.group();
////	        		out.add(Phenotype+"\t"+mat.group());
//	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
//	        	}
	        	
//	        	Sentence = Sentence.replace("associated with", "associated_with");
//	        	if(pheno.toLowerCase().contains("recurrence")) {
//        		System.out.println(pheno);
//        	}
//        	
//    		String[] words = Sentence.split(" ");
//    		int i = searchedWord(Sentence, "associated_with");
//    		int j = searchedWord(Sentence, "when");
//    		if(i!=-1&&j!=-1&&pheno.equals(".")) {
//    			String output = words[i+1];
//    			for (int k=i+2; k<j; k++) {
//    				output = output+" "+words[k];
//    			}
//    			if((output.toLowerCase().contains("induced")&&!output.contains("ADP"))||output.toLowerCase().contains("toxicity")||output.toLowerCase().contains("adverse")) {
//    				out.add(Annotation_ID+"\tToxicity\t"+output);
//    			}
//    			else if(output.contains("reaction")||output.contains("respon")||output.toLowerCase().contains("dose")||output.toLowerCase().contains("dosa")||output.toLowerCase().contains("treatment")||output.toLowerCase().contains("therapy")||output.toLowerCase().contains("resistance")||output.toLowerCase().contains("exposure")||output.toLowerCase().contains("discontinuation")||output.toLowerCase().contains("sensitivity")) {
//    				out.add(Annotation_ID+"\tTreatment\t"+output+"\tTreatment");
//    			}
//    			else if(output.toLowerCase().contains("pharmacokinetics")||output.contains("PK")||output.toLowerCase().contains("metabolism")||output.toLowerCase().contains("clearance")||output.toLowerCase().contains("concentration")||output.toLowerCase().contains("half-life")||output.toLowerCase().contains("uptake")) {
//    				out.add(Annotation_ID+"\tPharmacokinetics\t"+output+"\tPharmacokinetics");
//    			}
//    			else if(output.contains("CHEM$")) {
//    				out.add(Annotation_ID+"\tCHEM\t"+output+"\tCHEM");
//    			}
//    			else if(output.contains("GENO$")) {
//    				System.out.println(pheno);
//    				out.add(Annotation_ID+"\tGENO\t"+output);
//    			}
//    			else if((output.toLowerCase().contains("activity")&&!output.toLowerCase().contains("disease activity"))||output.toLowerCase().contains("affinity")||output.toLowerCase().contains("expression")||output.toLowerCase().contains("formation")||output.toLowerCase().contains("glucuronidation")||output.toLowerCase().contains("inhibition")||output.toLowerCase().contains("protein stability")||output.toLowerCase().contains("steady-state level")||output.toLowerCase().contains("sulfation")||output.toLowerCase().contains("transcription")||output.toLowerCase().contains("transport")) {
//    				System.out.println(pheno);
//    				out.add(Annotation_ID+"\tFunctional_activity\t"+output);
//    			}
//    			else out.add(Annotation_ID+"\t\t"+output);
//    		}
//    		else if(i!=-1&&pheno.equals(".")) {
//    			String output = words[i+1];
//    			if(words.length>i+3) {
//    				output = output+" "+words[i+2]+" "+words[i+3];
//    			}
//    			else if(words.length>i+2) {
//    				output = output+" "+words[i+2];
//    			}
//    			
//       			if((output.toLowerCase().contains("induced")&&!output.contains("ADP"))||output.toLowerCase().contains("toxicity")||output.toLowerCase().contains("adverse")) {
//    				out.add(Annotation_ID+"\tToxicity\t"+output);
//    			}
//    			else if(output.contains("reaction")||output.contains("respon")||output.toLowerCase().contains("dose")||output.toLowerCase().contains("dosa")||output.toLowerCase().contains("treatment")||output.toLowerCase().contains("therapy")||output.toLowerCase().contains("resistance")||output.toLowerCase().contains("exposure")||output.toLowerCase().contains("discontinuation")||output.toLowerCase().contains("sensitivity")) {
//    				out.add(Annotation_ID+"\tTreatment\t"+output+"\tTreatment");
//    			}
//    			else if(output.toLowerCase().contains("pharmacokinetics")||output.contains("PK")||output.toLowerCase().contains("metabolism")||output.toLowerCase().contains("clearance")||output.toLowerCase().contains("concentration")||output.toLowerCase().contains("half-life")||output.toLowerCase().contains("uptake")) {
//    				out.add(Annotation_ID+"\tPharmacokinetics\t"+output+"\tPharmacokinetics");
//    			}
//    			else if(output.contains("CHEM$")) {
//    				out.add(Annotation_ID+"\tCHEM\t"+output+"\tCHEM");
//    			}
//    			else if(output.contains("GENO$")) {
//    				System.out.println(pheno);
//    				out.add(Annotation_ID+"\tGENO\t"+output);
//    			}
//    			else if((output.toLowerCase().contains("activity")&&!output.toLowerCase().contains("disease activity"))||output.toLowerCase().contains("affinity")||output.toLowerCase().contains("expression")||output.toLowerCase().contains("formation")||output.toLowerCase().contains("glucuronidation")||output.toLowerCase().contains("inhibition")||output.toLowerCase().contains("protein stability")||output.toLowerCase().contains("steady-state level")||output.toLowerCase().contains("sulfation")||output.toLowerCase().contains("transcription")||output.toLowerCase().contains("transport")) {
//    				System.out.println(pheno);
//    				out.add(Annotation_ID+"\tFunctional_activity\t"+output);
//    			}
//    			else out.add(Annotation_ID+"\t\t"+output);
//    		}
//    		else if(pheno.equals(".")) {
//    			out.add(Annotation_ID+"\t"+Sentence);
//    		}
    		
//        	pat = Pattern.compile("\\|(GENO|POPU|CHEM)\\$ (protein|mRNA|cells|cell|dependence)");
//			mat = pat.matcher(Sentence);
//        	while(mat.find()) {
//        		if(mat.group(2).equals("protein")||mat.group(2).equals("mRNA")) {
//        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|GENO$");
//        		}
//        		else if(mat.group(2).equals("dependence")) {
//        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|DISE$");
//        		}
//        		else if(mat.group(2).equals("cells")||mat.group(2).equals("cell")) {
//        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|POPU$");
//        		}
//        	}
        	
	        	pat = Pattern.compile("\\|(GENO|POPU|CHEM)\\$ (protein|mRNA|cells|cell|dependence)");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(mat.group(2).equals("protein")||mat.group(2).equals("mRNA")) {
	        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|CHEM$");
	        		}
	        		else if(mat.group(2).equals("dependence")) {
	        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|DISE$");
	        		}
	        		else if(mat.group(2).equals("cells")||mat.group(2).equals("cell")) {
	        			Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|POPU$");
	        		}
	        	}
	        	
	        	String population = ".";
	        	
	        	//va_drug_ann
        		pat = Pattern.compile("\\bin (?i)(children Lymphoma T-Cell|human liver microsomes|Breast Cancer Cell Lines|([a-z]{1,})\\s([a-z]{1,})?\\s?case(s)?|(non)?smokers|healthy individuals|a person|people|elderly adult|children|women|men|(ICU )?patients|infants)?( with)?\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(mat.group(1)!=null) {
//	        			out.add(mat.group(1));
	        			population = mat.group(1);
		        		Sentence = Sentence.replace(population, "$"+population.replace(" ", "_")+"|POPU$");
	        		}
	        	}

	        	//va_fa_ann additional
//        		pat = Pattern.compile("\\b(?i)(human liver cytosol|muscle cells|liver kidney samples|liver samples|liver cells|fetal liver microsomes|liver microsomes|liver tissue B-lymphocytes|allelic isoenzyme purified from baculovirus-mediated insect cells|transfected neonatal rat cardiomyocytes|pancreatic cell lines|pancreatic islet cells|chinese hamster ovary cells|cancer tissues|CD56\\+ NK cells CD4\\+ T-helper cells|chinese hamster ovary cells|GIST882 cells|graft liver cell|H446 cells|HapMal LCLs|HepG2 liver cell line|human liver tissue|intestinal cell|liver|male liver samples|NCI60 cell lines|insect microsomes|pancreatic cell lines|pancreatic islet cells|primary tumor tissue|HEK cells|lymphoblast cell lines|erythrocytes|yeast system|yeast microsomes heterologously expressing|yeast microsomes|yeast cells|yeast|xenopus oocytes|whole blood RNA|whole blood gastric cells|whole blood from healthy volunteers|whole blood but not gastric cells|UB/OC1 cells|transfected human hepatoma cell lines|transfected CHO cells|Sf9 insect cells transfected with|Sf21 insect cells|red blood cells (RBC)|red blood cells|plasma|peripheral blood mononuclear cells|peripheral blood|PBMCs|NSCLC tissue samples|normal colon mucosa cells|normal breast tissue|NA18967 cells|myotubes|muscle|microsomes from insect cells Sf21|mice|lymphocytes|lymphoblasts from pediatric ALL patients|lymphoblastoid cell lines|lung tissue|LLC-PK1 cells|liver samples|liver kidney samples|liver cells|liver|LCLs derived from participants|K562 cells|insect cell microsomes|human umbilical cord T cells|human microsomes|human livers|human liver samples|human liver microsome samples|human liver cells|human liver|human hepatoma cells|human hepatocytes|human bronchial epithelial cells (CFBE41o-)|human bronchial epithelial cells|Huh7 hepatoma cells|HepG2 HEK293 cells|HepG2 cells|Hepa-1 group-B mutant cells|HeLa cells|HEK293T cells transfected with|HEK-293 cells dysgenic myotubes|HEK-293 cells|HEK293 cells|HEK 293 cells myotubes|HEK 293 cells|HEK 293 cells|HEI-OC1 cells|HCT116 cells|HapMap LCLs|HapMap cells|gastric cells|FRT cell lines|erythrocyte lysates|E.coli|E. coli membrane|E. coli DH5alpha|E. coli|COS-7 microsomes|COS-7 cells|cos-7 cell|COS-1 insect cells|COS-1 cells|COS cells|colonic mucosa of colorectal cancer patients|CFBEo- cells|CEU YRI cell lines|CEPH cell lines|breast tissue|BHK cells|before-treatment blood samples from pediatric asthma patients|B1642 cells|293FT cells|293 FT cells|transfected cells|tumor biopsy tissue|red blood cell lysates|pRBC|oocytes|microsomes from baculovirus-transfected cells|lymphoblastic cell lines|human jejunum homogenates|HLMs|erythrocyte lysate assays|CHO cells|cells)\\b");
//    			mat = pat.matcher(Sentence);
//	        	while(mat.find()) {
//	        		if(mat.group(1)!=null) {
////	        			out.add(mat.group());
//	        			population = mat.group();
//		        		Sentence = Sentence.replace(population, "$"+population.replace(" ", "_")+"|POPU$");
//	        		}
//	        	}
	        	
	        	String condition = ".";
        		pat = Pattern.compile("POPU\\$ with ([\\s'A-Za-z,-]{1,})( as)?");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(mat.group(1)!=null) {
//	        			out.add(mat.group(1).replace(" as compared to", ""));
	        			condition = mat.group(1).replace(" as compared to", "").trim();
		        		Sentence = Sentence.replace(condition, "$"+condition.replace(",","_").replace(" ", "_")+"|DISE$");
	        		}
	        	}

	        	if(condition.equals(".")) {
	        		pat = Pattern.compile("CHEM\\$ in ([\\s'A-Za-z,-]{1,}) as");
	    			mat = pat.matcher(Sentence);
		        	while(mat.find()) {
		        		if(mat.group(1)!=null) {
		        			condition = mat.group(1);
			        		Sentence = Sentence.replace(condition, "$"+condition.replace(",","_").replace(" ", "_")+"|DISE$");
		        		}
		        	}
	        	}
	        	
	        	pat = Pattern.compile("POPU\\$ ([A-Za-z\\s]{1,}) as");
    			mat = pat.matcher(Sentence);
    			while(mat.find()) {
	        		if(mat.group(1)!=null) {
	        			condition = mat.group(1);
		        		Sentence = Sentence.replace(condition, "$"+condition.replace(",","_").replace(" ", "_")+"|DISE$");
	        		}
	        	}
    			
    			pat = Pattern.compile("\\|GENO\\$ ([A-Za-z\\s]{1,}) activity");
    			mat = pat.matcher(Sentence);
    			while(mat.find()) {
	        		if(mat.group(1)!=null) {
	        			condition = mat.group();
		        		Sentence = Sentence.replace(mat.group(), condition.replace(",","").replace("|GENO$", "").replace(" ", "_")+"|GENO$");
	        		}
	        	}
    			
    			pat = Pattern.compile("\\b(non-small-cell lung cancer tumors)\\b");
    		   	mat = pat.matcher(Sentence);
    	    	while(mat.find()) {
    	    		Sentence = Sentence.replace(mat.group(),"$"+mat.group().replace(", ","_").replace(" ","_")+"|DISE$");
    	    	}
    	    	
	        	String geno_mod = ".";
        		pat = Pattern.compile("\\b([a-z]{3,})?( |-)?(deficiency|acetylator|activity|metabolizer|metabolizers)( phenotype)?\\b");
        		mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		geno_mod = mat.group().trim();
	        		Sentence = Sentence.replace(mat.group().trim(),"$"+mat.group().trim().replace(" ","_")+"|GENOMOD$");
	        	}
	        	
    			Sentence = Sentence.replace("","").replace("$CYP2D6|GENO$ $allelic_isoenzyme_","$CYP2D6_allelic_isoenzyme_").replace("HepG2$HEK293","$HepG2_and_HEK293").replace("|POPU$ (CFBE41o-)","_(CFBE41o-)|POPU$").replace("|CHEM$ -N+-glucuronide","-N+-glucuronide|CHEM$").replace("poor $","$poor_and_").replace("intermediate $","$intermediate_and_").replace("CYP2A6 normal,but not reduced,$","$CYP2A6_normal_").replace("CYP2A6 reduced,but not normal,$","$CYP2A6_reduced_").replace("|CHEM$ $(TNF-alpha)|GENO$ inhibitors","_(TNF-alpha)_inhibitors|CHEM$").replace("$warfarin|CHEM$ maintenance treatment","$warfarin_maintenance_treatment|DISE$").replace("$treatment_for|DISE$ $heroin|CHEM$ addiction","$treatment_for_heroin_addiction|DISE$").replace("|DISE$ (INR) of 2.0-3.0","_(INR)_of_2.0-3.0|DISE$").replace("Mitochondrial Diseases","$Mitochondrial_Diseases|DISE$").replace("[S-(E)]-2-ethylidene-1,5-dimethyl-3,3-diphenyl-pyrrolidine (S-EDDP)","$[S-(E)]-2-ethylidene-1,5-dimethyl-3,3-diphenyl-pyrrolidine_(S-EDDP)|CHEM$").replace("$children|POPU$ Lymphoma,T-Cell","$children_Lymphoma,T-Cell|POPU$").replace("$ Attention Deficit Disorder with $", "$ $Attention_Deficit_Disorder_with_").replace("|CHEM$ channel blockers", "_channel_blockers|CHEM$").replace("_$", "_").replace("-$", "-");
    	    	
    			pat = Pattern.compile("\\|([A-Z]+)\\$([A-Za-z0-9_*+-]{1,})");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		Sentence = Sentence.replace(mat.group(), mat.group(2)+"|"+mat.group(1)+"$");
	        	}

	        	pat = Pattern.compile("\\|(GENO|GENOMOD)\\$ \\$([A-Za-z0-9,_*/+()':-]{1,})\\|(GENO|GENOMOD)\\$");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		Sentence = Sentence.replace(mat.group(), "_"+mat.group(2)+"|GENO$");
	        	}
	        	
    			while(Sentence.contains("|CHEM$|GENO$")) {
	        		Sentence = Sentence.replace("|CHEM$|GENO$", "|CHEM$");
	        	}
    			while(Sentence.contains("|DISE$|CHEM$")) {
    				Sentence = Sentence.replace("|DISE$|CHEM$", "|CHEM$");
    			}
    			while(Sentence.contains("|DISE$|PHENO$")) {
    				Sentence = Sentence.replace("|DISE$|PHENO$", "|PHENO$");
    			}
	        	while(Sentence.contains("|GENOMOD$|PHENO$")) {
	        		Sentence = Sentence.replace("|GENOMOD$|PHENO$", "|PHENO$");
	        	}
	        	while(Sentence.contains("|GENO$|GENO$")) {
	        		Sentence = Sentence.replace("|GENO$|GENO$", "|GENO$");
	        	}
    			while(Sentence.contains("|CHEM$|CHEM$")) {
	        		Sentence = Sentence.replace("|CHEM$|CHEM$", "|CHEM$");
	        	}
	        	while(Sentence.contains("|PHENO$|PHENO$")) {
	        		Sentence = Sentence.replace("|PHENO$|PHENO$", "|PHENO$");
	        	}
	        	while(Sentence.contains("|POPU$|POPU$")) {
	        		Sentence = Sentence.replace("|POPU$|POPU$", "|POPU$");
	        	}
	        	while(Sentence.contains("|DISE$|DISE$")) {
	        		Sentence = Sentence.replace("|DISE$|DISE$", "|DISE$");
	        	}
	        	while(Sentence.contains("$$")) {
	        		Sentence = Sentence.replace("$$", "$");
	        	}
	        	
//	        	System.out.println(Sentence);
	        	String sem = getSem(Sentence);
	        	out.add(Annotation_ID+"\t"+Gene+"\t"+Chemical+"\t"+Phenotype+"\t"+Sentence+"\t"+aspect+"\t"+pheno+"\t"+condition+"\t"+population+"\t"+sem);
	        }
	    }
	    
   }
 
   public static void getGene(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {

	        	String gene = ".";
	        	
	        	for(String g:genes) {
	        		g = g.replace("-", " ");
	        		if(line.contains(g+" ")) {
	        			if(gene.equals(".")) {
	        				gene = g;
	            		}
	        			else if(!gene.contains(g)){
	            			gene = gene+","+g;
	            		}
	        		}
	        	}
	        	
	        	out.add(gene);
	        }
	    }
   }

   public static void getMed(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
 	    
	        while ((line = br.readLine()) != null) {

	        	String med = ".";
	        	
	        	for(String m:meds) {
	        		m = m.replace("-", " ");
	        		if(line.contains(m)) {
	        			if(med.equals(".")) {
	        				med = m;
	            		}
	            		else if(!med.contains(m)){
	            			med = med+","+m;
	            		}
	        		}
	        		
	        		m = m.toLowerCase();
	        		if(line.contains(m)) {
	        			if(med.equals(".")) {
	        				med = m;
	            		}
	        			else if(!med.contains(m)){
	            			med = med+","+m;
	            		}
	        		}
	        	}
	        	
	        	out.add(med);
	        }
	    }
  }
   
   public static void countWords(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	for(String s:line.split(",")) {
	        		out.add(s);
	        	}
	        }
	    }
   }
   
   public static void countType(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	   int activity = 0;
	   int affinity = 0;
	   int catalytic_activity = 0;
	   int clearance = 0;
	   int clinical_benefit = 0;
	   int concentration = 0;
	   int concentrations = 0;
	   int discontinuation = 0;
	   int disease_free_survival = 0;
	   int dose = 0;
	   int doses = 0;
	   int enzyme_activity = 0;
	   int event_free_survival = 0;
	   int exposed = 0;
	   int exposure = 0;
	   int express = 0;
	   int expressed = 0;
	   int expresses = 0;
	   int expression = 0;
	   int formation = 0;
	   int half_life = 0;
	   int inhibition = 0;
	   int intolerance = 0;
	   int level = 0;
	   int likelihood = 0;
	   int median_survival = 0;
	   int metabolism = 0;
	   int overall_survival = 0;
	   int prognosis = 0;
	   int prognostic = 0;
	   int progression = 0;
	   int progression_free_survival = 0;
	   int protein_stability = 0;
	   int recurrence = 0;
	   int recurrence_free_survival = 0;
	   int reduction = 0;
	   int resistance = 0;
	   int resistant = 0;
	   int respond = 0;
	   int responded = 0;
	   int response = 0;
	   int responses = 0;
	   int risk = 0;
	   int sensitive = 0;
	   int sensitivity = 0;
	   int severity = 0;
	   int survival = 0;
	   int time_to_tumor_recurrence = 0;
	   int transcribed = 0;
	   int transcription = 0;
	   int transport = 0;
	   int uptake = 0;
	   
	   int Treatments = 0;
	   int Genes_and_Gene_Products = 0;
	   int Procedures = 0;
	   int Concepts = 0;
	   int Function = 0;
	   int Living_Beings = 0;
	   int Human = 0;
	   int Disorders = 0;
	   int Activities = 0;
	   int Organizations = 0;
	   int Chemicals = 0;
	   int Anatomy = 0;
	   int Disease_Model = 0;
	   int Physiology = 0;
	   int Pathway = 0;
	   int Objects = 0;
	   int Drug_Phenotype = 0;
	   int Occupations = 0;
	   int Environmental_Exposure = 0;
	   
	   int a = 0; //2020
	   int b = 0; //2019
	   int c = 0; //2018
	   int d = 0; //2017
	   int e = 0; //2016
	   int f = 0; //2015
	   
	   try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	String[] l = line.split(",");
	        	for(String x:l) {
	        		if(x.equals("activity")){activity++;}
	        		if(x.equals("affinity")){affinity++;}
	        		if(x.equals("catalytic activity")){catalytic_activity++;}
	        		if(x.equals("clearance")){clearance++;}
	        		if(x.equals("clinical benefit")){clinical_benefit++;}
	        		if(x.equals("concentration")){concentration++;}
	        		if(x.equals("concentrations")){concentrations++;}
	        		if(x.equals("discontinuation")){discontinuation++;}
	        		if(x.equals("disease free survival")){disease_free_survival++;}
	        		if(x.equals("dose")){dose++;}
	        		if(x.equals("doses")){doses++;}
	        		if(x.equals("enzyme activity")){enzyme_activity++;}
	        		if(x.equals("event free survival")){event_free_survival++;}
	        		if(x.equals("exposed")){exposed++;}
	        		if(x.equals("exposure")){exposure++;}
	        		if(x.equals("express")){express++;}
	        		if(x.equals("expressed")){expressed++;}
	        		if(x.equals("expresses")){expresses++;}
	        		if(x.equals("expression")){expression++;}
	        		if(x.equals("formation")){formation++;}
	        		if(x.equals("half life")){half_life++;}
	        		if(x.equals("inhibition")){inhibition++;}
	        		if(x.equals("intolerance")){intolerance++;}
	        		if(x.equals("level")){level++;}
	        		if(x.equals("likelihood")){likelihood++;}
	        		if(x.equals("median survival")){median_survival++;}
	        		if(x.equals("metabolism")){metabolism++;}
	        		if(x.equals("overall survival")){overall_survival++;}
	        		if(x.equals("prognosis")){prognosis++;}
	        		if(x.equals("prognostic")){prognostic++;}
	        		if(x.equals("progression")){progression++;}
	        		if(x.equals("progression free survival")){progression_free_survival++;}
	        		if(x.equals("protein stability")){protein_stability++;}
	        		if(x.equals("recurrence")){recurrence++;}
	        		if(x.equals("recurrence free survival")){recurrence_free_survival++;}
	        		if(x.equals("reduction")){reduction++;}
	        		if(x.equals("resistance")){resistance++;}
	        		if(x.equals("resistant")){resistant++;}
	        		if(x.equals("respond")){respond++;}
	        		if(x.equals("responded")){responded++;}
	        		if(x.equals("response")){response++;}
	        		if(x.equals("responses")){responses++;}
	        		if(x.equals("risk")){risk++;}
	        		if(x.equals("sensitive")){sensitive++;}
	        		if(x.equals("sensitivity")){sensitivity++;}
	        		if(x.equals("severity")){severity++;}
	        		if(x.equals("survival")){survival++;}
	        		if(x.equals("time to tumor recurrence")){time_to_tumor_recurrence++;}
	        		if(x.equals("transcribed")){transcribed++;}
	        		if(x.equals("transcription")){transcription++;}
	        		if(x.equals("transport")){transport++;}
	        		if(x.equals("uptake")){uptake++;}
	        		
	        		if(x.equals("Treatments")){Treatments++;}
	        		if(x.equals("Genes and Gene Products")){Genes_and_Gene_Products++;}
	        		if(x.equals("Procedures")){Procedures++;}
	        		if(x.equals("Concepts")){Concepts++;}
	        		if(x.equals("Function")){Function++;}
	        		if(x.equals("Living Beings")){Living_Beings++;}
	        		if(x.equals("Human")){Human++;}
	        		if(x.equals("Disorders")){Disorders++;}
	        		if(x.equals("Activities")){Activities++;}
	        		if(x.equals("Organizations")){Organizations++;}
	        		if(x.equals("Chemicals")){Chemicals++;}
	        		if(x.equals("Anatomy")){Anatomy++;}
	        		if(x.equals("Disease Model")){Disease_Model++;}
	        		if(x.equals("Physiology")){Physiology++;}
	        		if(x.equals("Pathway")){Pathway++;}
	        		if(x.equals("Objects")){Objects++;}
	        		if(x.equals("Drug Phenotype")){Drug_Phenotype++;}
	        		if(x.equals("Occupations")){Occupations++;}
	        		if(x.equals("Environmental Exposure")){Environmental_Exposure++;}
	        	
	        		if(line.endsWith("/20")) {a++;}
	        		if(line.endsWith("/19")) {b++;}
	        		if(line.endsWith("/18")) {c++;}
	        		if(line.endsWith("/17")) {d++;}
	        		if(line.endsWith("/16")) {e++;}
	        		if(line.endsWith("/15")) {f++;}
	        	}
	        }
	    }
	    out.add(Integer.toString(activity));
	    out.add(Integer.toString(affinity));
	    out.add(Integer.toString(catalytic_activity));
	    out.add(Integer.toString(clearance));
	    out.add(Integer.toString(clinical_benefit));
	    out.add(Integer.toString(concentration));
	    out.add(Integer.toString(concentrations));
	    out.add(Integer.toString(discontinuation));
	    out.add(Integer.toString(disease_free_survival));
	    out.add(Integer.toString(dose));
	    out.add(Integer.toString(doses));
	    out.add(Integer.toString(enzyme_activity));
	    out.add(Integer.toString(event_free_survival));
	    out.add(Integer.toString(exposed));
	    out.add(Integer.toString(exposure));
	    out.add(Integer.toString(express));
	    out.add(Integer.toString(expressed));
	    out.add(Integer.toString(expresses));
	    out.add(Integer.toString(expression));
	    out.add(Integer.toString(formation));
	    out.add(Integer.toString(half_life));
	    out.add(Integer.toString(inhibition));
	    out.add(Integer.toString(intolerance));
	    out.add(Integer.toString(level));
	    out.add(Integer.toString(likelihood));
	    out.add(Integer.toString(median_survival));
	    out.add(Integer.toString(metabolism));
	    out.add(Integer.toString(overall_survival));
	    out.add(Integer.toString(prognosis));
	    out.add(Integer.toString(prognostic));
	    out.add(Integer.toString(progression));
	    out.add(Integer.toString(progression_free_survival));
	    out.add(Integer.toString(protein_stability));
	    out.add(Integer.toString(recurrence));
	    out.add(Integer.toString(recurrence_free_survival));
	    out.add(Integer.toString(reduction));
	    out.add(Integer.toString(resistance));
	    out.add(Integer.toString(resistant));
	    out.add(Integer.toString(respond));
	    out.add(Integer.toString(responded));
	    out.add(Integer.toString(response));
	    out.add(Integer.toString(responses));
	    out.add(Integer.toString(risk));
	    out.add(Integer.toString(sensitive));
	    out.add(Integer.toString(sensitivity));
	    out.add(Integer.toString(severity));
	    out.add(Integer.toString(survival));
	    out.add(Integer.toString(time_to_tumor_recurrence));
	    out.add(Integer.toString(transcribed));
	    out.add(Integer.toString(transcription));
	    out.add(Integer.toString(transport));
	    out.add(Integer.toString(uptake));
	    
//	    out.add(Integer.toString(Treatments));
//	    out.add(Integer.toString(Genes_and_Gene_Products));
//	    out.add(Integer.toString(Procedures));
//	    out.add(Integer.toString(Concepts));
//	    out.add(Integer.toString(Function));
//	    out.add(Integer.toString(Living_Beings));
//	    out.add(Integer.toString(Human));
//	    out.add(Integer.toString(Disorders));
//	    out.add(Integer.toString(Activities));
//	    out.add(Integer.toString(Organizations));
//	    out.add(Integer.toString(Chemicals));
//	    out.add(Integer.toString(Anatomy));
//	    out.add(Integer.toString(Disease_Model));
//	    out.add(Integer.toString(Physiology));
//	    out.add(Integer.toString(Pathway));
//	    out.add(Integer.toString(Objects));
//	    out.add(Integer.toString(Drug_Phenotype));
//	    out.add(Integer.toString(Occupations));
//	    out.add(Integer.toString(Environmental_Exposure));
   }
   
   public static void UMLSCategoy(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	   id.put("acty", "Activities");
	   id.put("bhvr", "Activities");
	   id.put("dora", "Activities");
	   id.put("evnt", "Activities");
	   id.put("gora", "Activities");
	   id.put("inbe", "Activities");
	   id.put("mcha", "Activities");
	   id.put("ocac", "Activities");
	   id.put("socb", "Activities");
	   id.put("anst", "Anatomy");
	   id.put("blor", "Anatomy");
	   id.put("bpoc", "Anatomy");
	   id.put("bsoj", "Anatomy");
	   id.put("bdsu", "Anatomy");
	   id.put("bdsy", "Anatomy");
	   id.put("cell", "Anatomy");
	   id.put("celc", "Anatomy");
	   id.put("emst", "Anatomy");
	   id.put("ffas", "Anatomy");
	   id.put("tisu", "Anatomy");
	   id.put("aapp", "Genes and Gene Products");
	   id.put("antb", "Treatments");
	   id.put("bacs", "Chemicals");
	   id.put("bodm", "Chemicals");
	   id.put("chem", "Chemicals");
	   id.put("chvf", "Chemicals");
	   id.put("chvs", "Chemicals");
	   id.put("clnd", "Treatments");
	   id.put("elii", "Chemicals");
	   id.put("enzy", "Genes and Gene Products");
	   id.put("hops", "Environmental Exposure");
	   id.put("horm", "Treatments");
	   id.put("imft", "Treatments");
	   id.put("irda", "Chemicals");
	   id.put("inch", "Chemicals");
	   id.put("nnon", "Genes and Gene Products");
	   id.put("orch", "Treatments");
	   id.put("phsu", "Treatments");
	   id.put("rcpt", "Genes and Gene Products");
	   id.put("vita", "Chemicals");
	   id.put("clas", "Concepts");
	   id.put("cnce", "Concepts");
	   id.put("ftcn", "Function");
	   id.put("grpa", "Concepts");
	   id.put("idcn", "Concepts");
	   id.put("inpr", "Concepts");
	   id.put("lang", "Concepts");
	   id.put("qlco", "Concepts");
	   id.put("qnco", "Concepts");
	   id.put("rnlw", "Concepts");
	   id.put("spco", "Concepts");
	   id.put("tmco", "Concepts");
	   id.put("drdd", "Devices");
	   id.put("medd", "Devices");
	   id.put("resd", "Devices");
	   id.put("acab", "Disorders");
	   id.put("anab", "Disorders");
	   id.put("comd", "Disorders");
	   id.put("cgab", "Disorders");
	   id.put("dsyn", "Disorders");
	   id.put("emod", "Disease Model");
	   id.put("fndg", "Disorders");
	   id.put("inpo", "Environmental Exposure");
	   id.put("mobd", "Disorders");
	   id.put("neop", "Disorders");
	   id.put("patf", "Disorders");
	   id.put("sosy", "Disorders");
	   id.put("amas", "Genes and Gene Products");
	   id.put("crbs", "Genes and Gene Products");
	   id.put("gngm", "Genes and Gene Products");
	   id.put("mosq", "Genes and Gene Products");
	   id.put("nusq", "Genes and Gene Products");
	   id.put("geoa", "Geographic Areas");
	   id.put("aggp", "Human");
	   id.put("amph", "Disease Model");
	   id.put("anim", "Disease Model");
	   id.put("arch", "Living Beings");
	   id.put("bact", "Living Beings");
	   id.put("bird", "Disease Model");
	   id.put("euka", "Living Beings");
	   id.put("famg", "Human");
	   id.put("fish", "Disease Model");
	   id.put("fngs", "Disease Model");
	   id.put("grup", "Living Beings");
	   id.put("humn", "Human");
	   id.put("mamm", "Disease Model");
	   id.put("orgm", "Living Beings");
	   id.put("podg", "Human");
	   id.put("plnt", "Living Beings");
	   id.put("popg", "Human");
	   id.put("prog", "Human");
	   id.put("rept", "Disease Model");
	   id.put("vtbt", "Disease Model");
	   id.put("virs", "Living Beings");
	   id.put("enty", "Objects");
	   id.put("food", "Objects");
	   id.put("mnob", "Objects");
	   id.put("phob", "Objects");
	   id.put("sbst", "Objects");
	   id.put("bmod", "Occupations");
	   id.put("ocdi", "Occupations");
	   id.put("hcro", "Organizations");
	   id.put("orgt", "Organizations");
	   id.put("pros", "Organizations");
	   id.put("shro", "Organizations");
	   id.put("biof", "Function");
	   id.put("eehu", "Environmental Exposure");
	   id.put("hcpp", "Environmental Exposure");
	   id.put("lbtr", "Physiology");
	   id.put("npop", "Function");
	   id.put("phpr", "Function");
	   id.put("celf", "Function");
	   id.put("clna", "Physiology");
	   id.put("genf", "Function");
	   id.put("menp", "Activities");
	   id.put("moft", "Function");
	   id.put("ortf", "Physiology");
	   id.put("orga", "Physiology");
	   id.put("orgf", "Physiology");
	   id.put("phsf", "Physiology");
	   id.put("diap", "Procedures");
	   id.put("edac", "Procedures");
	   id.put("hlca", "Procedures");
	   id.put("lbpr", "Procedures");
	   id.put("mbrt", "Procedures");
	   id.put("resa", "Procedures");
	   id.put("topp", "Procedures");
	   id.put("path", "Pathway");
	   id.put("pheno", "Drug Phenotype");
	   
	   try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
 	    
	        while ((line = br.readLine()) != null) {
	        	
	        	System.out.println(line);
	        	
	        	String[] sem = line.split(",");
	        	String output = id.get(sem[0]);
	        	
	        	for(int i=1; i<sem.length; i++) {
	        		output = output +","+ id.get(sem[i]);
	        	}
	        	
	        	out.add(output);
	        }
	    }
   }
   public static void varAnnUMLS(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	System.out.println(line);
	        	String[] match = line.split("\t")[0].split(",");
	        	String[] sem = line.split("\t")[1].split(",");
	        	String[] pheno = line.split("\t")[2].split(",");
	        	System.out.println(Integer.toString(match.length)+"\t"+Integer.toString(sem.length));
	        	String match1 = "."; String sem1 = "."; String pheno1 = ".";  

        		for(int i=0; i<match.length; i++) {
    	        	if(match[i].equals("clinical")&&i<match.length-1) {
    	        		if(match[i+1].equals("benefit")) {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i]+"_"+match[i+1];
        	        			sem1 = "pheno";
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i]+"_"+match[i+1];
        	        			sem1 = sem1+",pheno";
        	        		}
        	        		i++;
    	        		}
    	        		else {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = sem[i];
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+","+sem[i];
        	        		}
    	        		}
    	        	}
    	        	else if(match[i].equals("overall")&&i<match.length-1) {
    	        		if(match[i+1].equals("survival")) {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i]+"_"+match[i+1];
        	        			sem1 = "pheno";
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i]+"_"+match[i+1];
        	        			sem1 = sem1+",pheno";
        	        		}
        	        		i++;
    	        		}
    	        		else {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = sem[i];
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+","+sem[i];
        	        		}
    	        		}
    	        	}
    	        	else if(match[i].equals("TIME")&&i<match.length-1) {
    	        		if(match[i+1].equals("tumor_recurrence")) {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i]+"_to_"+match[i+1];
        	        			sem1 = "pheno";
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i]+"_to_"+match[i+1];
        	        			sem1 = sem1+",pheno";
        	        		}
        	        		i++;
    	        		}
    	        		else {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = sem[i];
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+","+sem[i];
        	        		}
    	        		}
    	        	}
    	        	else if(match[i].equals("disease")&&i<match.length-1) {
    	        		if(match[i+1].equals("free")) {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i]+"_"+match[i+1]+"_survival";
        	        			sem1 = "pheno";
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i]+"_"+match[i+1]+"_survival";
        	        			sem1 = sem1+",pheno";
        	        		}
        	        		i++;
    	        		}
    	        		else {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = sem[i];
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+","+sem[i];
        	        		}
    	        		}
    	        	}
    	        	else if(match[i].equals("median_survival_time")) {
    	        		if(match1.equals(".")) {
    	        			match1 = "median_survival";
    	        			sem1 = "pheno";
    	        		}
    	        		else {
    	        			match1 = match1+",median_survival";
    	        			sem1 = sem1+",pheno";
    	        		}
    	        	}
    	        	else if(match[i].equals("progression_free_survival")||match[i].equals("recurrence_free_survival")||match[i].equals("event_free_survival")) {
    	        		if(match1.equals(".")) {
    	        			match1 = match[i];
    	        			sem1 = "pheno";
    	        		}
    	        		else {
    	        			match1 = match1+","+match[i];
    	        			sem1 = sem1+",pheno";
    	        		}
    	        	}
    	        	else if(match[i].contains("pathway")||match[i].contains("signaling")) {
    	        		if(match1.equals(".")) {
    	        			match1 = match[i];
    	        			sem1 = "path";
    	        		}
    	        		else {
    	        			match1 = match1+","+match[i];
    	        			sem1 = sem1+",path";
    	        		}
    	        	}
    	        	else {
    	        		String matched = "N";
    	        		for(String p:pheno) {
    	        			if(match[i].contains(p)) {
    	        				matched = "Y";
    	        			}
    	        		}
    	        		
    	        		if(matched.equals("Y")) {
    	        			if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = "pheno";
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+",pheno";
        	        		}	
    	        		}
    	        		else if(!match[i].equals("")) {
	        				if(match1.equals(".")) {
        	        			match1 = match[i];
        	        			sem1 = sem[i];
        	        		}
        	        		else {
        	        			match1 = match1+","+match[i];
        	        			sem1 = sem1+","+sem[i];;
        	        		}
	        			}
    	        	}
    	        	
	        	}
	        	
	        	out.add(Integer.toString(match.length)+"\t"+Integer.toString(sem.length)+"\t"+match1+"\t"+sem1);
	        }
	    }
   }
   
   public static void varAnnFoundation(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
   	    
	        while ((line = br.readLine()) != null) {
	        	String Sentence = line;
	        
//	        	System.out.println(Sentence);
	        	
	        	String pheno = ".";
	        	String aspect = ".";
	        	String population = ".";
	        	
	        	//va_drug_ann
        		Pattern pat = Pattern.compile("\\b(decreased|increased|reduced|positive|poorer|better|worse|shorter|longer)\\b");
    			Matcher mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(aspect.equals(".")) {
	        			aspect = mat.group().trim();
	        		}
	        		else if(!aspect.contains(mat.group().trim())) {
	        			aspect = aspect+","+mat.group().trim();
	        		}
	        		System.out.println(aspect);
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|ASPT$");
	        	}
        	
	        	pat = Pattern.compile("\\b(steady-state |trough |non-|ultra-)?(clinical benefit|dose(s|d)?|dosage|response(s)?|respond(ed)?|metabolism|metabolize(s|d)?|clearance|concentration(s)?|resistance|resistant|exposure|expose(s|d)?|discontinue(s|d)?|discontinuation|expression|express(es|ed)?|transcription|transcribe(s|d)?|sensitivity|sensitive|glucoruonidation|sulfation|inhibition|formation|half(-| )?life|level|transport|uptake|activity|affinity|catalytic activity|enzyme activity|protein stability|intolerability|intolerance|AUC|disease free survival|event free survival|median survival|overall survival|progression free survival|recurrence free survival|survival|likelihood|prognostic|prognosis|progression|time to tumor progression|reduction|risk|severity|recurrence|time to tumor recurrence)\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(pheno.equals(".")) {
	        			pheno = mat.group().trim();
	        		}
	        		else if(!pheno.contains(mat.group().trim())) {
	        			pheno = pheno+","+mat.group().trim();
	        		}
	        		System.out.println(pheno);
//	        		out.add(Phenotype+"\t"+mat.group());
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
	        	}
	        	
	        	//va_drug_ann
        		pat = Pattern.compile("\\b(?i)(([a-z0-9]{3,})\\s([a-z0-9]{3,})?\\s?(T-|B-)?cell|([a-z0-9]{3,})\\s([a-z0-9]{3,})?\\s?(cell line|case|protein|mrna)|(non)?smoker|healthy individual|a person|people|elderly adult|children|women|men|(ICU )?patient|infant)(s)?\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(population.equals(".")) {
	        			population = mat.group().trim();
	        		}
	        		else if(!population.contains(mat.group().trim())) {
	        			population = population+","+mat.group().trim();
	        		}

	        		Sentence = Sentence.replace(population, "$"+population.replace(" ", "_")+"|POPU$");
	        	}

	        	//va_fa_ann additional
//        		pat = Pattern.compile("\\b(?i)(human liver cytosol|muscle cells|liver kidney samples|liver samples|liver cells|fetal liver microsomes|liver microsomes|liver tissue B-lymphocytes|allelic isoenzyme purified from baculovirus-mediated insect cells|transfected neonatal rat cardiomyocytes|pancreatic cell lines|pancreatic islet cells|chinese hamster ovary cells|cancer tissues|CD56\\+ NK cells CD4\\+ T-helper cells|chinese hamster ovary cells|GIST882 cells|graft liver cell|H446 cells|HapMal LCLs|HepG2 liver cell line|human liver tissue|intestinal cell|liver|male liver samples|NCI60 cell lines|insect microsomes|pancreatic cell lines|pancreatic islet cells|primary tumor tissue|HEK cells|lymphoblast cell lines|erythrocytes|yeast system|yeast microsomes heterologously expressing|yeast microsomes|yeast cells|yeast|xenopus oocytes|whole blood RNA|whole blood gastric cells|whole blood from healthy volunteers|whole blood but not gastric cells|UB/OC1 cells|transfected human hepatoma cell lines|transfected CHO cells|Sf9 insect cells transfected with|Sf21 insect cells|red blood cells (RBC)|red blood cells|plasma|peripheral blood mononuclear cells|peripheral blood|PBMCs|NSCLC tissue samples|normal colon mucosa cells|normal breast tissue|NA18967 cells|myotubes|muscle|microsomes from insect cells Sf21|mice|lymphocytes|lymphoblasts from pediatric ALL patients|lymphoblastoid cell lines|lung tissue|LLC-PK1 cells|liver samples|liver kidney samples|liver cells|liver|LCLs derived from participants|K562 cells|insect cell microsomes|human umbilical cord T cells|human microsomes|human livers|human liver samples|human liver microsome samples|human liver cells|human liver|human hepatoma cells|human hepatocytes|human bronchial epithelial cells (CFBE41o-)|human bronchial epithelial cells|Huh7 hepatoma cells|HepG2 HEK293 cells|HepG2 cells|Hepa-1 group-B mutant cells|HeLa cells|HEK293T cells transfected with|HEK-293 cells dysgenic myotubes|HEK-293 cells|HEK293 cells|HEK 293 cells myotubes|HEK 293 cells|HEK 293 cells|HEI-OC1 cells|HCT116 cells|HapMap LCLs|HapMap cells|gastric cells|FRT cell lines|erythrocyte lysates|E.coli|E. coli membrane|E. coli DH5alpha|E. coli|COS-7 microsomes|COS-7 cells|cos-7 cell|COS-1 insect cells|COS-1 cells|COS cells|colonic mucosa of colorectal cancer patients|CFBEo- cells|CEU YRI cell lines|CEPH cell lines|breast tissue|BHK cells|before-treatment blood samples from pediatric asthma patients|B1642 cells|293FT cells|293 FT cells|transfected cells|tumor biopsy tissue|red blood cell lysates|pRBC|oocytes|microsomes from baculovirus-transfected cells|lymphoblastic cell lines|human jejunum homogenates|HLMs|erythrocyte lysate assays|CHO cells|cells)\\b");
//    			mat = pat.matcher(Sentence);
//	        	while(mat.find()) {
//	        		if(mat.group(1)!=null) {
////	        			out.add(mat.group());
//	        			population = mat.group();
//		        		Sentence = Sentence.replace(population, "$"+population.replace(" ", "_")+"|POPU$");
//	        		}
//	        	}
	        	
	        	while(Sentence.contains("$$")) {
	        		Sentence = Sentence.replace("$$", "$");
	        	}
	        	while(Sentence.contains("|ASPT$|ASPT$")) {
	        		Sentence = Sentence.replace("|ASPT$|ASPT$", "|ASPT$");
	        	}
	        	while(Sentence.contains("|POPU$|POPU$")) {
	        		Sentence = Sentence.replace("|POPU$|POPU$", "|POPU$");
	        	}
	        	while(Sentence.contains("|PHENO$|PHENO$")) {
	        		Sentence = Sentence.replace("|PHENO$|PHENO$", "|PHENO$");
	        	}
//	        	System.out.println(Sentence);
//	        	String sem = getSem(Sentence);
//	        	out.add(Sentence+"\t"+aspect+"\t"+pheno+"\t"+population);
	        	out.add(pheno);
	        }
	    }
   }

public static void varAnnPheno(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	   	try (BufferedReader br1 = new BufferedReader(new FileReader(folder+"\\phenotypes\\phenotypes.tsv"))) {
	   		String line1 = "";
	        while ((line1 = br1.readLine()) != null) {
	        	String Name = line1.split("\t")[1];
	        	if(Name.equals("Child")||Name.equals("Young Child")) {
	        		continue;
	        	}
	        	id.put(Name.trim(), Name.trim());
	        	if(line1.split("\t").length>2&&!line1.split("\t")[2].equals("")) {
		        	String[] Alternate_Names = line1.split("\t")[2].replaceAll(",\"", "|").replaceAll("\"", "").split("\\|");
		        	for(String a : Alternate_Names) {
		        		if(a.trim().equals("DR")) {
			        		continue;
			        	}
		        		id.put(a.trim(), Name.trim());
		        	}
	        	}
	        }
		}
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	String Annotation_ID = line.split("\t")[0];
	        	String Gene = line.split("\t")[2].replace("\"", "");
	        	String Chemical = line.split("\t")[3].replace("\"", "");
	        	String Phenotype = line.split("\t")[5].replace("\"", "");
	        	String Sentence = line.split("\t")[8].replace(" + ", "+").replace(" *", "*").replaceAll("\\b(genotype|genotypes|Genotypes)\\b", "Genotype").replace("allele", "Allele");
	        	String Genotype = "";
	        	if(line.split("\t").length>10) {
	        		Genotype = line.split("\t")[10].replace(" + ", "+").replace(" *", "*");
	        	}
	        	
	        	if(Sentence.endsWith(".")) {
	        		Sentence = Sentence.substring(0, Sentence.length()-1);
				}
	        	
	        	String output = Annotation_ID+"\t"+Gene+"\t"+Chemical+"\t"+Phenotype+"\t"+Sentence;
	        	
        		Pattern pat = Pattern.compile("\\b(is |are )(not )?associated with \\b");
    			Matcher mat = pat.matcher(Sentence);
    			String associated = ".";
    			while(mat.find()) {
    				associated = mat.group();
    				Sentence = Sentence.replace(mat.group(), "|");
    			}
	        	
	        	//geno is associated with
	        	String geno = Sentence.split("\\|")[0].replace(" ", "_").trim();
	        	if(Sentence.split("\\|").length>1) {
	        		Sentence = Sentence.split("\\|")[1].trim();
	        	}
	        	
	        	pat = Pattern.compile("\\bas compared to \\b");
    			mat = pat.matcher(Sentence);
    			String compared = ".";
    			while(mat.find()) {
    				compared = mat.group();
    				Sentence = Sentence.replace(mat.group(), "|");
    			}
    			
        		String geno1 = ".";
	        	if(Sentence.split("\\|").length>1) {
	        		geno1 = Sentence.split("\\|")[1].trim().replace(" ", "_");
	        	}
	        	Sentence = Sentence.split("\\|")[0].trim();
	        	
	        	pat = Pattern.compile("\\b(when )?(treated|exposed|assayed) (with|to) \\b");
    			mat = pat.matcher(Sentence);
    			String treated = ".";
    			while(mat.find()) {
    				treated = mat.group();
    				Sentence = Sentence.replace(mat.group(), "|");
    			}
    			String chemical = ".";
    			if(Sentence.split("\\|").length>1) {
    				chemical = Sentence.split("\\|")[1].trim();
				}
    			Sentence = Sentence.split("\\|")[0].trim();
    			
	        	//in people with
    			pat = Pattern.compile("\\bin ([a-z]{1,} )?((non)?smoker(s)?|individual(s)?|patient(s)?|a person|people|adult(s)?|child(ren)?|women|men|woman|man|infant(s)?|vitro|user(s)?)( with)?\\s?\\b");
    			mat = pat.matcher(chemical);
    			String population = ".";
    			String disease = ".";
    			while(mat.find()) {
    				population = mat.group().trim();
    				if(chemical.replace(mat.group(), "|").split("\\|").length>1) {
    					disease = chemical.replace(mat.group(), "|").split("\\|")[1];
    				}
    				chemical = chemical.replace(mat.group(), "|").split("\\|")[0].trim();
    			}
    			
        		pat = Pattern.compile("\\bin ([a-z]{1,} )?((non)?smoker(s)?|individual(s)?|patient(s)?|a person|people|adult(s)?|child(ren)?|women|men|woman|man|infant(s)?|vitro|user(s)?)( with)?\\s?\\b");
    			mat = pat.matcher(Sentence);
    			while(mat.find()) {
    				if(population.equals(".")) {
    					population = mat.group().trim();
    				}
    				else if(!population.contains(mat.group().trim())) {
    					population = population+";"+mat.group().trim();
    				}
    				if(Sentence.replace(mat.group(), "|").split("\\|").length>1) {
    					if(disease.equals(".")) {
    						disease = Sentence.replace(mat.group(), "|").split("\\|")[1];
        				}
        				else if(!disease.contains(Sentence.replace(mat.group(), "|").split("\\|")[1])) {
        					disease = disease+";"+Sentence.replace(mat.group(), "|").split("\\|")[1];
        				}
    				}
	        		Sentence = Sentence.replace(mat.group(), "|").split("\\|")[0].trim();
    			}
    			
				//va_pheno_ann
	        	String pheno = ".";
	        	String aspect = ".";
	        	String condition = ".";
        		pat = Pattern.compile("\\b(better |earlier |faster |greater |higher |larger |longer |lower |poorer |shorter |slower |smaller |stronger |decreased |delayed |diminished |enhanced |impaired |improved |increased |reduced |sustained )?([-_A-Za-z]{4,} )?(progression )?([-_A-Za-z]{4,} )?([-_A-Za-z]{4,})?(clinical benefit|dose|response|metabolism|clearance|concentration(s)?|activity|affinity|expression|formation|glucuronidation|half-life|inhibition|protein stability|sensitivity|steady-state level|sulfation|transcription|transport|uptake|resistance|exposure|discontinuation|intolerability|intolerance|prognosis|recurrence|AUC|reduction|survival|severity|likelihood|risk|progression)\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		if(mat.group(1)!=null) {
	        			aspect = mat.group(1).trim();
	        		}
	        		pheno = mat.group();
	        		Sentence = Sentence.replace(pheno, "$"+pheno.replace(" ", "_")+"|PHENO$");
	        	}
	        	
	        	while(Sentence.contains("$$")) {
	        		Sentence = Sentence.replace("$$", "$");
	        	}
	        	while(Sentence.contains("|PHENO$|PHENO$")) {
	        		Sentence = Sentence.replace("|PHENO$|PHENO$", "|PHENO$");
	        	}
	        	
	        	if(!Sentence.startsWith("$")&&Sentence.contains("$")) {
	        		pat = Pattern.compile("\\b(better |earlier |faster |greater |higher |larger |longer |lower |poorer |shorter |slower |smaller |stronger |decreased |delayed |diminished |enhanced |impaired |improved |increased |reduced |sustained )([A-Za-z0-9,_*-/+\\(\\)\\[\\]\\s':]{1,})\\$\\b");
	    			mat = pat.matcher(Sentence);
	    			while(mat.find()) {
	        			aspect = mat.group().split(" ")[0];
	        			pheno = mat.group().replace("$", "")+pheno;
	        			Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace("$", "").replace(" ", "_"));
	        		}
	    			
	    			String[] words = Sentence.split(" ");
	    			condition = words[0];
					for(int i=1; i<words.length; i++) {
						condition = condition + " " + words[i];
					}
					
					condition = annotateChemical(condition, Chemical);
		        	
					for(int i = 0; i<5; i++) {
						condition = annotateDISE(condition);
//		        		if(disease.equals(".")) {
//		        			disease = condition.split("\t")[1];
//		        		}
//		        		else if(!disease.contains(condition.split("\t")[1])) {
//		        			disease = disease+","+condition.split("\t")[1];
//		        		}
		        		condition = condition.split("\t")[0];
		     	    }
	        	}
	        	else if(!Sentence.startsWith("$")&&!Sentence.contains("$")) {
	        		String[] words = Sentence.split(" ");
	        		if(words.length<2) {
	        			continue;
	        		}
	        		if(words[0].equals("better")||words[0].equals("earlier")||words[0].equals("faster")||words[0].equals("greater")||words[0].equals("higher")||words[0].equals("larger")||words[0].equals("longer")||words[0].equals("lower")||words[0].equals("poorer")||words[0].equals("shorter")||words[0].equals("slower")||words[0].equals("smaller")||words[0].equals("stronger")||words[0].equals("decreased")||words[0].equals("delayed")||words[0].equals("diminished")||words[0].equals("enhanced")||words[0].equals("impaired")||words[0].equals("improved")||words[0].equals("increased")||words[0].equals("reduced")||words[0].equals("sustained")) {
	        			aspect = words[0];
	        		}
	        		condition = words[1];
					for(int i=2; i<words.length; i++) {
						condition = condition + " " + words[i];
					}
					
					condition = annotateChemical(condition, Chemical);
		        	
					for(int i = 0; i<5; i++) {
						condition = annotateDISE(condition);
//		        		if(disease.equals(".")) {
//		        			disease = condition.split("\t")[1];
//		        		}
//		        		else if(!disease.contains(condition.split("\t")[1])) {
//		        			disease = disease+","+condition.split("\t")[1];
//		        		}
		        		condition = condition.split("\t")[0];
		     	    }
//					condition = "$"+condition.replace(",", "_").replace(" ", "_")+"|COND$";
	        	}
	        	else {
	        		Sentence = annotateChemical(Sentence, Chemical);
		        	
					for(int i = 0; i<5; i++) {
						Sentence = annotateDISE(Sentence);
		        		if(disease.equals(".")) {
		        			disease = Sentence.split("\t")[1];
		        		}
		        		else if(!disease.contains(Sentence.split("\t")[1])) {
		        			disease = disease+","+Sentence.split("\t")[1];
		        		}
		        		Sentence = Sentence.split("\t")[0];
		     	    }
	        	}
//	        	System.out.println(condition);
	        	out.add(output+"\t"+geno+"\t"+associated+"\t"+aspect+"\t"+pheno+"\t"+condition+"\t"+population+"\t"+disease+"\t"+treated+"\t"+chemical+"\t"+compared+"\t"+geno1);
	        }
	    }
   }
   public static void clinicalAnn(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
  	    
	        while ((line = br.readLine()) != null) {
	        	String Annotation_ID = line.split("\t")[0];
	        	String Genotype = line.split("\t")[1];
	        	String Sentence = line.split("\t")[2].replace("\"", "").split("\\.")[0].replace("Failureas", "Failures").replace("metabolizer genotype", "metabolizer").replace(" + ", "+").replace(" *", "*").replaceAll("\\b(genotype|genotypes|Genotypes)\\b", "Genotype").replace("allele", "Allele");
//	        	String Phenotype = line.split("\t")[3].replace("\"", "");
	        	String Gene = line.split("\t")[4].replace("\"", "");
	        	
        		Pattern pat = Pattern.compile("\\bThere is [a-z]{1,}?\\s?no\\b");
    			Matcher mat = pat.matcher(Sentence);
	        	
	        	if(Sentence.startsWith("No")) {
	        		out.add(".");
	        		continue;
	        	}
//	        	else if(mat.find()) {
//	        		continue;
//	        	}
//	        	else if(Sentence.startsWith("In vitro")) {
//	        		continue;
//	        	}
	        	
	        	//GENO
	        	Sentence = annotateGenotype(Sentence, Genotype, Gene);
	        	
	        	//CHEM
	        	Sentence = annotateChemical(Sentence, "");
	        	
	        	//POPU
        		pat = Pattern.compile("\\b(?i)(adolescent|cell|children|individual|male|men|patient|people|smoker|subject|women)s?\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
//	        		out.add(mat.group());
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|POPU$");
	        	}
	        	
	        	//PHENO-drug
        		pat = Pattern.compile("\\b(decreased |increased |reduced |positive |poorer |better |worse |shorter |longer )?(steady-state |trough |treatment )?(clinical benefit|dose|response|metabolism|clearance|concentration(s)?|resistance|exposure|discontinuation)\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
	        	}
	        	
	        	//PHENO-fa
        		pat = Pattern.compile("\\b(decreased |increased |reduced |positive |poorer |better |worse |shorter |longer )?(activity|affinity|catalytic activity|clearance|concentrations|enzyme activity|expression|formation|glucuronidation|half-life|inhibition|metabolism|protein stability|sensitivity|steady-state level|sulfation|transcription|transport|uptake)\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
	        	}
	        	
	        	//PHENO-pheno
        		pat = Pattern.compile("\\b(decreased |increased |reduced |positive |poorer |better |worse |shorter |longer )?(intolerability|intolerance|progression|prognosis|(?i)((time(-| )to(-| )tumor )?recurrence)|AUC|reduction|(?i)((overall |(event|disease|progression|recurrence)(-| )free |median )?survival)|severity|likelihood|risk)\\b");
    			mat = pat.matcher(Sentence);
	        	while(mat.find()) {
	        		Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|PHENO$");
	        	}
	        	
	        	while(Sentence.contains("$s|")) {
	        		Sentence = Sentence.replace("$s|", "$|");
	        	}
    			while(Sentence.contains("|GENO$|GENO$")) {
	        		Sentence = Sentence.replace("|GENO$|GENO$", "|GENO$");
	        	}
	        	while(Sentence.contains("|PHENO$|PHENO$")) {
	        		Sentence = Sentence.replace("|PHENO$|PHENO$", "|PHENO$");
	        	}
	        	while(Sentence.contains("|POPU$|POPU$")) {
	        		Sentence = Sentence.replace("|POPU$|POPU$", "|POPU$");
	        	}
	        	while(Sentence.contains("|DISE$|DISE$")) {
	        		Sentence = Sentence.replace("|DISE$|DISE$", "|DISE$");
	        	}
	        	while(Sentence.contains("$$")) {
	        		Sentence = Sentence.replace("$$", "$");
	        	}
	        	
	        	String sem = getSem(Sentence);
//	        	Sentence = Sentence.replace("with", "\t").replace("who", "\t");
//	        	System.out.println(Sentence);
	        	out.add(Annotation_ID+"\t"+Sentence+"\t"+sem);
//	        	if(Sentence.split("\t")[0].split(" ").length<4) {
//	        		out.add(Sentence.split("\t")[0]+"\t"+Sentence.split("\t")[0].split(" ").length);
//	        	}
	        }
	    }
   }
   
   public static String annotateGenotype(String Sentence, String Genotype, String Gene) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
		
	   	Pattern pat = Pattern.compile("\\(PA[0-9]+\\)");
	   	Matcher mat = pat.matcher(Gene);
	   	while(mat.find()) {
	   		Gene = Gene.replace(mat.group(), "");
	   	}
	   	
		Sentence = Sentence.replace(Genotype.replace("allele", "Allele"), Genotype.replace("allele", "Allele").replace("' ", "'").replace(" ", "_"));
		Genotype = Genotype.replace("allele", "Allele").replace("' ", "'").replace(" ", "_");
		
   		String[] words = Sentence.split(" ");
		String output = ""; String add = "";
		
		int i = -1; 
		if(Sentence.contains(Genotype)) {
			words = Sentence.split(" ");
			i = searchedWord(Sentence, Genotype);
			if(i!=-1&&i!=words.length-1) {
				String Allele = Genotype;
				if(words[i+1].equals("Genotype")||words[i+1].equals("Allele")) {
					Allele = Allele+" "+words[i+1];
				}
				else if((words[i-1].equals("Genotype")||words[i-1].equals("Allele")||words[i-1].equals("SLC6A4"))&&i!=0) {
					Allele = words[i-1]+" "+Allele;
				}
				Sentence = Sentence.replace(Allele, "$"+Allele.replace(" ", "_")+"|GENO$");
			}
			else if(i==words.length-1) {
				String Allele = Genotype;
				if(words[i-1].equals("Genotype")||words[i-1].equals("Allele")) {
					Allele = words[i-1]+" "+Allele;
				}
				Sentence = Sentence.replace(Allele, "$"+Allele.replace(" ", "_")+"|GENO$");
			}
		}

		output = "";
		words = Sentence.replace("BP ALU", "BP_ALU").split(" ");
		for(int j=0; j<words.length; j++) {
			if(j==words.length-2&&(words[j].equals("Genotype")||words[j].equals("Allele"))) {
				output = output+" $"+words[j]+"_"+words[j+1]+"|GENO$";
				j++;
			}
			else if(j<words.length-3&(words[j].equals("Allele")||words[j].equals("Genotype"))&&(words[j+2].equals("(assigned"))) {
				output = output+" $"+words[j]+"_"+words[j+1]+"|GENO$";
				j++;
			}
			else if(words[j].contains("Genotype")) {
				output = output+" $"+words[j]+"|GENO$";
			}
			else if(words[j].equals("SLC6A4")) {
				Genotype = words[j];
				for(int k=j+1; k<words.length; k++) {
					Genotype = Genotype+"_"+words[k];
					j++;
				}
			}
			else if(!words[j].equals("and")&&!words[j].equals("or")) {
				output = output+" "+words[j];
			}
		}
		Sentence = output.trim();

		output = "";
		words = Sentence.split(" ");
		if(!Gene.equals("")) {
			String[] Genes = Gene.split(",");
			for(int j=0; j<words.length; j++) {
				add = "";
				for(String g:Genes) {
					if(words[j].contains(g.trim())) {
						add = "Y";
					}
				}
				
				if(j==words.length-2&&add.equals("Y")) {
					output = output+" $"+words[j]+"_"+words[j+1]+"|GENO$";
					j++;
				}
				else if(add.equals("Y")) {
					output = output+" $"+words[j]+"|GENO$";
				}
				else {
					output = output+" "+words[j];
				}
			}
			Sentence = output.trim();
		}

		words = Sentence.split(" ");
   		output = "";
   		for(String w:words) {
   			if(w.equals("ABCA1")||w.equals("ABCB1")||w.equals("ABCB9")||w.equals("ABCC1")||w.equals("ABCC10")||w.equals("ABCD1")||w.equals("ABCD2")||w.equals("ABCD3")||w.equals("ABCG2")||w.equals("AGPAT2")||w.equals("ARRB2")||w.equals("C14orf49")||w.equals("CES1")||w.equals("CETP")||w.equals("CXCL8")||w.equals("CYP1A1")||w.equals("CYP1B1")||w.equals("CYP2B6")||w.equals("CYP2C19")||w.equals("CYP2D6")||w.equals("CYP3A")||w.equals("CYP3A4")||w.equals("CYP3A5")||w.equals("CYP4F11")||w.equals("CYP4F12")||w.equals("CYP4F2")||w.equals("DPYD")||w.equals("ERCC1")||w.equals("HEK293")||w.equals("IFNAR1")||w.equals("IL12RB2")||w.equals("IL17A")||w.equals("IL17RA")||w.equals("IL1B")||w.equals("IL1R2")||w.equals("LDLR")||w.equals("MIR133A1")||w.equals("MIR2052")||w.equals("MIRLET7I")||w.equals("MKI67")||w.equals("MRP1")||w.equals("NR3C1")||w.equals("PRSS55")||w.equals("SAE1")||w.equals("SCAP")||w.equals("TAP2")||w.equals("TBX2")||w.equals("TCL1A")||w.equals("TLR4")||w.equals("TPMT")||w.equals("TRAF1")||w.equals("TRPC1")||w.equals("TRPC3")||w.equals("TRPC6")||w.equals("TYMS")||w.equals("UGT1A1")||w.equals("UGT1A9")||w.equals("UGT2B15")||w.equals("UGT2B17")||w.equals("UGT2B4")||w.equals("USP7")||w.equals("VKORC1")||w.equals("WNT5B")) {
   				output = output+"$"+w+"|GENO$";
   			}
   			else output = output+" "+w;
   		}
   		Sentence = output.trim();
   		
   		pat = Pattern.compile("\\brs[0-9]+\\b");
	   	mat = pat.matcher(Sentence);
	   	while(mat.find()) {
	   		Sentence = Sentence.replace(mat.group(), "$"+mat.group()+"|GENO$");
	   	}
	   	
		return Sentence;
   }

	   
   public static String annotateChemical(String Sentence, String Chemical) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	    Pattern pat = Pattern.compile("\\(PA[0-9]+\\)");
	   	Matcher mat = pat.matcher(Chemical);
	   	while(mat.find()) {
	   		Chemical = Chemical.replace(mat.group(), ")");
	   	}
	   	Chemical = Chemical.replace("),",";");
	   			
	   	if(!Chemical.equals("")) {
	   		Chemical = Chemical.substring(0, Chemical.length()-1);
	   		for(String c:Chemical.split(";")){
	   			String cap = c.substring(0, 1).toUpperCase() + c.substring(1);
	   			String low = c.substring(0, 1).toLowerCase() + c.substring(1);
				if(Sentence.contains(c.trim())&&!Sentence.contains("$"+c.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$")) {
					Sentence = Sentence.replace(c.trim(), "$"+c.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$");
				}
				else if(Sentence.contains(cap.trim())&&!Sentence.contains("$"+cap.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$")) {
					Sentence = Sentence.replace(cap.trim(), "$"+cap.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$");
				}
				else if(Sentence.contains(low.trim())&&!Sentence.contains("$"+low.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$")) {
					Sentence = Sentence.replace(low.trim(), "$"+low.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$");
				}
			}
	   	}
	   	
		//CHEM-va-drug
		pat = Pattern.compile("\\b(?i)(active metabolite|angiotensin ii|anthracyclines related substances|antineoplastic|ar c124910xx|artemisinin derivatives|clopidogrel active metabolite|desmethyl|hdl cholesterol|insulin recombinant zinc acetate|low density lipoprotein|n-desethyl|o-desmethyl-tramadol|other general anesthetics volatile anesthetics|simvastatin acid|thioguanosine diphosphate|thioguanosine monophosphate|thioguanosine triphosphate|urea derivatives|uric acid|vitamin b-complex incl. combinations|vitamin d analogues)\\b");
		mat = pat.matcher(Sentence);
		while(mat.find()) {
//	   		out.add(mat.group());
			Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|CHEM$");
		}
		
		//CHEM-clinical
		pat = Pattern.compile("\\b(?i)(anti(-|\\s)?epileptic|anti(-|\\s)?depressant|anti(-|\\s)?psychotic|azathiopurine|diuretic|bisphosphonate|statin|thiopurine|glucocorticoid|anti(-|\\s)?TNF(-|\\s)?alpha|interferon(-|\\s)?alpha|interferon(-|\\s)?beta|beta(-|\\s)?blockers|antiretrovirals|beta2-antagonists|beta-2-agonists|beta-2-adenoreceptor agonists|sulfonylureas|antihypertensive|anthracyclines|adjuvant cyclophophamide|non-steroid(s)? anti-inflammatory|inhalational anaesthetics|antiretroviral|hormone replacement|amitryptiline|triptans|fluoropyrimidine-based chemotherapy|nifedepine|nifediping|antiepileptic|sulfonamides urea derivatives|antitubercular|anti-tubercular and antiretroviral|fluoropyrimidines|tissue plasminogen activator|co-trimoxazole|sulfonylurea|anti-tubercular|pegylated interferon|inhalational anesthetics|peginterferon-alpha|thiopurines|folinic acid|oral antidiabetes|antiretroviral therapy|anti-tuberculosis|peginterferon|tricyclic|fumaric acid|dalimumab|peginterferon alpha|delcetrapib|doxorubcin|peginterferon alfa|anti-tuberculosis|estrogen replacement|recombinant interferon|antiplatelet|arpiprazole|salvianolate|aromatase|reductase|cholinesterase|nucleoside|analog metabolite|angiotensin(-|\\s)?converting enzyme|selective serotonin(-|\\s)?reuptake|protease)\\s?(agents|inhibitors|drugs|treatment)?\\b");
		mat = pat.matcher(Sentence);
		while(mat.find()) {
			Sentence = Sentence.replace(mat.group(), "$"+mat.group().replace(" ", "_")+"|CHEM$");
		}
		
		//medication group
//	   	pat = Pattern.compile("\\b[a-z0-9-]{4,}?\\s?[a-z0-9-]{4,} (drugs|agents|derivatives|blockers|(ant)?agonists|inhibitors)\\b");
//		mat = pat.matcher(Sentence);
//	   	while(mat.find()) {
//	   		out.add(mat.group());
//	   	}
		
		//CHEM-va-all
		for(String c:chemicals){
			if(Sentence.contains(c.trim())&&!Sentence.contains("$"+c.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$")) {
				Sentence = Sentence.replace(c.trim(), "$"+c.trim().replace(", ", "_").replace(" ", "_")+"|CHEM$");
			}
		}
		
		while(Sentence.contains("|CHEM$|CHEM$")) {
			Sentence = Sentence.replace("|CHEM$|CHEM$", "|CHEM$");
		}
		while(Sentence.contains("_$")) {
			Sentence = Sentence.replace("_$", "_");
		}
		while(Sentence.contains("|CHEM$_")) {
			Sentence = Sentence.replace("|CHEM$_", "_");
		}
		while(Sentence.contains("_|CHEM$")) {
			Sentence = Sentence.replace("_|CHEM$", "|CHEM$ ");
		}
		while(Sentence.contains("$$")) {
    		Sentence = Sentence.replace("$$", "$");
    	}
		
		pat = Pattern.compile("([A-Za-z0-9_()-]{1,})\\$([A-Za-z0-9_()-]{1,})\\|CHEM\\$");
		mat = pat.matcher(Sentence);
		while(mat.find()) {
			if(!mat.group(1).equals("(")&&!mat.group(1).equals("-")&&!mat.group(1).equals("CHEM")) {
		   		Sentence = Sentence.replace(mat.group(), "$"+mat.group(1)+mat.group(2)+"|CHEM$");
			}
			if(mat.group(2).equals("s_1")||mat.group(2).equals("ether")) {
		   		Sentence = Sentence.replace(mat.group(), mat.group(1)+mat.group(2).replace("_", " "));
			}
		}
		while(Sentence.contains("$$")) {
    		Sentence = Sentence.replace("$$", "$");
    	}
		mat = pat.matcher(Sentence);
		while(mat.find()) {
			if(!mat.group(1).equals("(")&&!mat.group(1).equals("-")&&!mat.group(1).equals("CHEM")) {
		   		Sentence = Sentence.replace(mat.group(), "$"+mat.group(1)+mat.group(2)+"|CHEM$");
			}
			if(mat.group(2).equals("s_1")||mat.group(2).equals("ether")) {
		   		Sentence = Sentence.replace(mat.group(), mat.group(1)+mat.group(2).replace("_", " "));
			}
		}
		while(Sentence.contains("$$")) {
    		Sentence = Sentence.replace("$$", "$");
    	}

		pat = Pattern.compile("\\$([A-Za-z0-9_()-]{1,})\\|CHEM\\$([A-Za-z0-9_()-]{1,})");
		mat = pat.matcher(Sentence);
		while(mat.find()) {
			if(!mat.group(2).equals(")")) {
		   		Sentence = Sentence.replace(mat.group(), "$"+mat.group(1)+mat.group(2)+"|CHEM$");
			}
		}
		while(Sentence.contains("$$")) {
    		Sentence = Sentence.replace("$$", "$");
    	}
		mat = pat.matcher(Sentence);
		while(mat.find()) {
			if(!mat.group(2).equals(")")) {
		   		Sentence = Sentence.replace(mat.group(), "$"+mat.group(1)+mat.group(2)+"|CHEM$");
			}
		}
		while(Sentence.contains("$$")) {
    		Sentence = Sentence.replace("$$", "$");
    	}
		
		return Sentence;

   }

   public static String annotateDISE(String Sentence) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
	   String disease = ".";
	   for (Map.Entry<String,String> entry : id.entrySet()) {
	   		if(Sentence.contains(entry.getKey())) {
	   			if(disease.length()<entry.getKey().length()) {
	   				disease = entry.getKey();
	   			}
	   		}
	   	}
//	    System.out.println(disease);
	    if(!disease.equals(".")) {
		   	Sentence = Sentence.replace(disease,"$"+id.get(disease).replace(", ","_").replace(" ","_")+"|DISE$");
	    }
//	    System.out.println(Sentence);
	   	Pattern pat = Pattern.compile("\\b(non-small-cell lung cancer tumors)\\b");
	   	Matcher mat = pat.matcher(Sentence);
    	while(mat.find()) {
    		Sentence = Sentence.replace(mat.group(),"$"+mat.group().replace(", ","_").replace(" ","_")+"|DISE$");
    	}
		
		while(Sentence.contains("|DISE$|DISE$")) {
			Sentence = Sentence.replace("|DISE$|DISE$", "|DISE$");
		}
		while(Sentence.contains("_$")) {
			Sentence = Sentence.replace("_$", "_");
		}
		while(Sentence.contains("|DISE$_")) {
			Sentence = Sentence.replace("|DISE$_", "_");
		}
		while(Sentence.contains("_|DISE$")) {
			Sentence = Sentence.replace("_|DISE$", "|DISE$ ");
		}
		while(Sentence.contains("$$")) {
   		Sentence = Sentence.replace("$$", "$");
		}
		
    	pat = Pattern.compile("([A-Za-z]{1,})\\$([A-Za-z]{1,})\\|DISE\\$");
		mat = pat.matcher(Sentence);
		while(mat.find()) {
	   		Sentence = Sentence.replace(mat.group(), "$"+mat.group(1)+mat.group(2)+"|DISE$");
//	   		System.out.println(Sentence);
		}
		
		return Sentence+"\t"+disease;
   }
	 
   public static String getSem (String Sentence) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {

	   	String Sentence0 = Sentence;
	   	String sem = ""; String output = "";
	   	Pattern pat = Pattern.compile("\\$([A-Za-z0-9,_*-/+\\(\\)\\[\\]':]{1,})\\|([A-Z]+)\\$");
		Matcher mat = pat.matcher(Sentence0);
	   	while(mat.find()) {
	   		Sentence0 = Sentence0.replace(mat.group(), "");

	   		if(sem.equals("")) {
	   			if(mat.group(2).contains("GENO")){
	   				sem = "GENO";
	   			}
	   			else sem = mat.group(2);
	   		}
	   		else {
	   			if(mat.group(2).contains("GENO")){
	   				sem = sem + "," +"GENO";
	   			}
	   			else sem = sem + "," +mat.group(2);
	   		
	   		}
	   	}
	   	
	   	
   		Sentence0 = Sentence0.replaceAll("(is|are|when|as) (not )?(associated|compared|assayed|exposed|treated) (with|to)", "").replace("(assigned as ", "").replace(" phenotype", "").replace("  ", " ").trim();

   		String[] words = Sentence0.split(" ");
   		output = "";
   		for(String w:words) {
   			if(w.equals("in")||w.equals("of")||w.equals("to")||w.equals("with")) {
//   				output = output+" $";
   			}
   			else output = output+" "+w;
   		}
   		Sentence0 = output.replace("  ", " ").trim();
//   		out.add(output.replace("  ", " ").trim());
	   	
   	   	if(Sentence0.contains("$")) {
	   		System.out.println(Sentence);
	   		System.out.println(Sentence0);
	   	}
   	   	
	   	while(sem.contains(",CHEM,CHEM")) {
	   		sem = sem.replace(",CHEM,CHEM", ",CHEM");
	   	}
	   	while(sem.contains(",PHENO,PHENO")) {
	   		sem = sem.replace(",PHENO,PHENO", ",PHENO");
	   	}
	   	while(sem.contains("GENO,GENO")) {
	   		sem = sem.replace("GENO,GENO", "GENO");
	   	}
//	   	Sentence0 = output.trim();
	   	
	   	return Sentence0+"\t"+sem;
   }

public static void readTXT(String file) throws FileNotFoundException, IOException, SAXException, ParserConfigurationException {
    	
	    try (BufferedReader br = new BufferedReader(new FileReader(file))) {
	
	        String line = "";
	        String print = "N";
	        PrintWriter writer = null;
    		File[] listOfFiles = new File(folder).listFiles();
    	    int i =0;
    	    
//    	    for (int i = 0; i < listOfFiles.length; i++) {
    	        while ((line = br.readLine()) != null) {
    	        	
    	        	if(line.contains("<Assertion Type=\"confers")) {
    	        		print = "Y";
    	        		out.add(line);
    	        		i++;
//    	        		writer = new PrintWriter(folder+"ClinVar\\"+ id +".txt", "UTF-8");
    	        	}
    	        	else if(line.contains("<Attribute Type=")&&print.equals("Y")) {
    	        		out.add(line);
    	        		i++;
//    	        		writer = new PrintWriter(folder+"ClinVar\\"+ id +".txt", "UTF-8");
    	        	}
    	        	else if (line.contains("</ClinVarSet>")&&print.equals("Y")){
//    		        	writer.println(line.replaceAll("\\s{2,}", " "));
//    		        	writer.flush();
    	        		print = "N";
    	        	}
    	        	
    	        	if(i>10000) {
    	        		break;
	        		}
    	        }
//    	    }
	    }
    }
    
    public static void parseJSON(String file) throws FileNotFoundException, IOException, ParseException {
    	
		JSONParser jsonParser = new JSONParser();
		
		try (FileReader reader = new FileReader(file))
		{
            Object obj = jsonParser.parse(reader);

            JSONArray assertionList = (JSONArray) obj;
            
            for(Object as : assertionList) {
        		//Get patient object within list
        		JSONObject assertionObject = (JSONObject) as;
        		
        		//Get patient info
        		String name = assertionObject.get("name").toString();
        		String summary = assertionObject.get("description").toString().toLowerCase().replaceAll("\n", "");
//        		String summary = assertionObject.get("summary").toString().toLowerCase();
        		
        		JSONObject disease = (JSONObject) assertionObject.get("disease");
        		String disease_name = disease.get("name").toString();
        		if(summary.contains(disease_name.toLowerCase())||summary.contains(disease_name.toLowerCase().replace("receptor ", ""))) {
    				summary = summary.replace(disease_name.toLowerCase(), "$"+disease_name+"|DISE$");
    				if(summary.contains(disease_name.toLowerCase().replace("receptor ", ""))){
        				summary = summary.replace(disease_name.toLowerCase().replace("receptor ", ""), "$"+disease_name+"|DISE$");
    				}
        		}
        		
        		JSONObject variant = (JSONObject) assertionObject.get("variant");
        		String var_name = variant.get("name").toString();
        		JSONObject gene = (JSONObject) assertionObject.get("gene");
        		String gene_name = gene.get("name").toString().replace("ERBB", "HER");
        		if((summary.contains(var_name.toLowerCase())||summary.contains(var_name.toLowerCase().replace(" ", "-")))&&!var_name.contains(gene_name)) {
    				summary = summary.replace(var_name, "$"+var_name+"|VAR$");
    				if(summary.contains(var_name.toLowerCase().replace(" ", "-"))){
        				summary = summary.replace(var_name.toLowerCase().replace(" ", "-"), "$"+var_name+"|VAR$");
    				}
    				
    				if(summary.contains(gene_name.toLowerCase())) {
        				summary = summary.replace(gene_name.toLowerCase(), "$"+gene_name+"|GENE$");
            		}
        		}
        		else if(summary.contains(var_name.toLowerCase())||summary.contains(var_name.toLowerCase().replace(" ", "-"))) {
    				summary = summary.replace(var_name.toLowerCase(), "$"+var_name+"|VAR$");
    				if(summary.contains(var_name.toLowerCase().replace(" ", "-"))){
        				summary = summary.replace(var_name.toLowerCase().replace(" ", "-"), "$"+var_name+"|VAR$");
    				}
        		}
        		
        		Pattern pat = Pattern.compile("\\$([A-Z0-9]{1,})\\|GENE\\$([a-z0-9]{1,})");
	        	Matcher mat = pat.matcher(summary);

	            while (mat.find()) {
	            	summary = summary.replace(mat.group(), mat.group(1).toLowerCase()+mat.group(2)); 
	            }
	            
        		JSONArray drugs = (JSONArray) assertionObject.get("drugs");
        		String drug_name = "";
        		for(Object d : drugs) {
        			JSONObject drugObject = (JSONObject) d;
        			if(drug_name.equals("")) {
        				drug_name = drugObject.get("name").toString();
        			}
        			else drug_name = drug_name+","+drugObject.get("name").toString();
        			
        			summary = summary.replace(drugObject.get("name").toString().toLowerCase(), "$"+drugObject.get("name").toString()+"|MED$");
    				if(!summary.contains("MED$")){
        				summary = summary.replace(drugObject.get("name").toString().toLowerCase(), "$"+drugObject.get("name").toString()+"|MED$");
    				}
        		}
        		
        		String evidence_type = assertionObject.get("evidence_type").toString();
        		if(evidence_type.contains("Predict")) {
        			pat = Pattern.compile("(predict)([a-z]{0,})");
    	        	mat = pat.matcher(summary);

    	            while (mat.find()) {
    	            	summary = summary.replace(mat.group(), "$Predict|EV$"); 
    	            }
        		}
        		String evidence_direction = assertionObject.get("evidence_direction").toString();
        		String clinical_significance = assertionObject.get("clinical_significance").toString();
        		if(clinical_significance.contains("Sensitivity")) {
        			pat = Pattern.compile("(sensitiv)([a-z]{1,})");
    	        	mat = pat.matcher(summary);

    	            while (mat.find()) {
    	            	summary = summary.replace(mat.group(), "$Sensitive|CLIN$"); 
    	            }
        		}
        		else if(summary.contains(clinical_significance.toLowerCase())) {
    				summary = summary.replace(clinical_significance.toLowerCase(), "$"+clinical_significance+"|CLIN$");
        		}
        		
        		String fda_regulatory_approval = assertionObject.get("fda_regulatory_approval").toString();
        		
        		if(!drug_name.equals("")) {
            		System.out.println(name+"\t"+summary); 
                    out.add(name+"\t"+summary+"\t"+disease_name+"\t"+var_name+"\t"+gene_name+"\t"+drug_name+"\t"+evidence_type+"\t"+evidence_direction+"\t"+clinical_significance+"\t"+fda_regulatory_approval);
        		}
            }
        }
	}
    
	public static int searchedWord(String sentence, String searchedWord) {
		
	    if (sentence == null || searchedWord == null) throw new IllegalArgumentException("May not be null");
	    String[] words = sentence.split(" ");
	    int searchedIndex = -1;
	    for (int i=0; i<words.length; i++) {
	        if (words[i].equals(searchedWord)) searchedIndex = i;
	        if (searchedIndex!=-1) break;
	    }

	    int output = searchedIndex;
//	    System.out.println(output);
	    return output;
	}
	
    public static void printArrayListFile(ArrayList<String> _list, String _file) throws FileNotFoundException, UnsupportedEncodingException {

        try (PrintWriter writer = new PrintWriter(_file, "UTF-8")) {
            for (String str : _list) {
                writer.println(str);
                writer.flush();
            }
            writer.close();
        }

    }
    
	public static <T> void removeDuplicates(ArrayList<T> list) {
	    int size = list.size();
	    int out = 0;
	    {
	        final Set<T> encountered = new HashSet<T>();
	        for (int in = 0; in < size; in++) {
	            final T t = list.get(in);
	            final boolean first = encountered.add(t);
	            if (first) {
	                list.set(out++, t);
	            }
	        }
	    }
	    while (out < size) {
	        list.remove(--size);
	    }
	}
    
	public static void sort(String s[], int n) 
	{ 
	    for (int i=1 ;i<n; i++) 
	    { 
	        String temp = s[i]; 
	  
	        // Insert s[j] at its correct position 
	        int j = i - 1; 
	        while (j >= 0 && temp.length() < s[j].length()) 
	        { 
	            s[j+1] = s[j]; 
	            j--; 
	        } 
	        s[j+1] = temp; 
	    } 
	} 
}
